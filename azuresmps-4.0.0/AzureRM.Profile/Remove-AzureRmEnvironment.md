---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623196"
---
# <span data-ttu-id="d4507-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4507-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="d4507-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4507-102">SYNOPSIS</span></span>
<span data-ttu-id="d4507-103">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="d4507-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="d4507-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4507-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4507-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4507-105">DESCRIPTION</span></span>
<span data-ttu-id="d4507-106">Remove-AzureRmEnvironment Cmdlet 會移除端點和中繼資料資訊以連線至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="d4507-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="d4507-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4507-107">EXAMPLES</span></span>

### <span data-ttu-id="d4507-108">範例1：建立及移除測試環境</span><span class="sxs-lookup"><span data-stu-id="d4507-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="d4507-109">這個範例示範如何使用 [載入 AzureRmEnvironment] 建立環境，然後如何使用 [移除] AzureRmEnvironment 刪除環境。</span><span class="sxs-lookup"><span data-stu-id="d4507-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="d4507-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4507-110">PARAMETERS</span></span>

### <span data-ttu-id="d4507-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4507-111">-Name</span></span>
<span data-ttu-id="d4507-112">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="d4507-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4507-113">-確認</span><span class="sxs-lookup"><span data-stu-id="d4507-113">-Confirm</span></span>
<span data-ttu-id="d4507-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4507-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4507-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4507-115">-WhatIf</span></span>
<span data-ttu-id="d4507-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4507-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4507-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4507-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4507-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4507-118">CommonParameters</span></span>
<span data-ttu-id="d4507-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4507-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4507-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4507-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4507-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d4507-121">INPUTS</span></span>

## <span data-ttu-id="d4507-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d4507-122">OUTPUTS</span></span>

### <span data-ttu-id="d4507-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4507-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="d4507-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d4507-124">NOTES</span></span>

## <span data-ttu-id="d4507-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4507-125">RELATED LINKS</span></span>

[<span data-ttu-id="d4507-126">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4507-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="d4507-127">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4507-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="d4507-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4507-128">Set-AzureRMEnvironment</span></span>]()

