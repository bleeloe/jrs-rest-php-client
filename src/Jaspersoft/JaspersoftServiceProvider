<?php
/**
 * JasperSoftServiceProvider
 * Integrated jaspersoft with laravel 4.
 *
 * @author  harysutrisno@gmail.com
 */

namespace Jaspersoft;

use Illuminate\Support\ServiceProvider;

class JasperSoftServiceProvider extends ServiceProvider
{
    public function register()
    {
        $this->app->bind('jasperclient', function ($app) {

            try {
                return new \Jaspersoft\Client\Client($app['config']['jaspersoft.url'], $app['config']['jaspersoft.username'], $app['config']['jaspersoft.password'], $app['config']['jaspersoft.organization']);
            } catch (Exception $e) {
                return 'Connection failed to server report!';
            }

        });
    }
}
