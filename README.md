# Yii2 Bugsnag integration
To use, configure as such:

    $config = [
        'components' => [
            'errorHandler' => [
                'class' => 'jcherniak\yii2bugsnag\BugsnagErrorHandler'
            ],
            'bugsnag' => [
                'class' => 'jcherniak\yii2bugsnag\BugsnagComponent', // Or your override of such
                'bugsnag_api_key' => 'YOUR API KEY',
                'notifyReleaseStages' => ['staging', 'production'],
            ],
            'log' => [
                'traceLevel' => 8,
                'targets' => [
                    [
                        'class' => 'common\components\BugsnagLogTarget',
                        'levels' => ['error', 'warning', 'info', 'trace'],
                        'logVars' => [],
                    ]
                ],
            ],
        ],
    ];

