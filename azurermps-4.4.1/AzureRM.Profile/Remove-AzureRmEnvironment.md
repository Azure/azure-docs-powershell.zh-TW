---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: d27a05e652cbcd11d35536ebff97f04b3c60f520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626248"
---
# <span data-ttu-id="7026d-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="7026d-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="7026d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7026d-102">SYNOPSIS</span></span>
<span data-ttu-id="7026d-103">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="7026d-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7026d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7026d-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7026d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7026d-105">DESCRIPTION</span></span>
<span data-ttu-id="7026d-106">Remove-AzureRmEnvironment Cmdlet 會移除端點和中繼資料資訊以連線至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="7026d-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="7026d-107">示例</span><span class="sxs-lookup"><span data-stu-id="7026d-107">EXAMPLES</span></span>

### <span data-ttu-id="7026d-108">範例1：建立及移除測試環境</span><span class="sxs-lookup"><span data-stu-id="7026d-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="7026d-109">這個範例示範如何使用 [載入 AzureRmEnvironment] 建立環境，然後如何使用 [移除] AzureRmEnvironment 刪除環境。</span><span class="sxs-lookup"><span data-stu-id="7026d-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="7026d-110">參數</span><span class="sxs-lookup"><span data-stu-id="7026d-110">PARAMETERS</span></span>

### <span data-ttu-id="7026d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7026d-111">-DefaultProfile</span></span>
<span data-ttu-id="7026d-112">用於與 azure 進行通訊的認證、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="7026d-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7026d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7026d-113">-Name</span></span>
<span data-ttu-id="7026d-114">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="7026d-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7026d-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="7026d-115">-Scope</span></span>
<span data-ttu-id="7026d-116">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="7026d-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7026d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7026d-117">-Confirm</span></span>
<span data-ttu-id="7026d-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7026d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7026d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7026d-119">-WhatIf</span></span>
<span data-ttu-id="7026d-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7026d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7026d-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7026d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7026d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7026d-122">CommonParameters</span></span>
<span data-ttu-id="7026d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7026d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7026d-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7026d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7026d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7026d-125">INPUTS</span></span>

## <span data-ttu-id="7026d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7026d-126">OUTPUTS</span></span>

### <span data-ttu-id="7026d-127">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7026d-127">PSAzureEnvironment</span></span>

## <span data-ttu-id="7026d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7026d-128">NOTES</span></span>

## <span data-ttu-id="7026d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7026d-129">RELATED LINKS</span></span>

[<span data-ttu-id="7026d-130">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7026d-130">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="7026d-131">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7026d-131">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="7026d-132">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7026d-132">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

