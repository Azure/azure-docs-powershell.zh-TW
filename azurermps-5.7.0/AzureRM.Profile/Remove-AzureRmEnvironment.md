---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454179"
---
# <span data-ttu-id="3530b-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3530b-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="3530b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3530b-102">SYNOPSIS</span></span>
<span data-ttu-id="3530b-103">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="3530b-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3530b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3530b-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3530b-105">說明</span><span class="sxs-lookup"><span data-stu-id="3530b-105">DESCRIPTION</span></span>
<span data-ttu-id="3530b-106">Remove-AzureRmEnvironment Cmdlet 會移除端點和中繼資料資訊以連線至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="3530b-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="3530b-107">示例</span><span class="sxs-lookup"><span data-stu-id="3530b-107">EXAMPLES</span></span>

### <span data-ttu-id="3530b-108">範例1：建立及移除測試環境</span><span class="sxs-lookup"><span data-stu-id="3530b-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="3530b-109">這個範例示範如何使用 [載入 AzureRmEnvironment] 建立環境，然後如何使用 [移除] AzureRmEnvironment 刪除環境。</span><span class="sxs-lookup"><span data-stu-id="3530b-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="3530b-110">參數</span><span class="sxs-lookup"><span data-stu-id="3530b-110">PARAMETERS</span></span>

### <span data-ttu-id="3530b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3530b-111">-DefaultProfile</span></span>
<span data-ttu-id="3530b-112">用於與 azure 進行通訊的認證、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="3530b-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3530b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3530b-113">-Name</span></span>
<span data-ttu-id="3530b-114">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="3530b-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="3530b-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="3530b-115">-Scope</span></span>
<span data-ttu-id="3530b-116">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="3530b-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3530b-117">-確認</span><span class="sxs-lookup"><span data-stu-id="3530b-117">-Confirm</span></span>
<span data-ttu-id="3530b-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3530b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3530b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3530b-119">-WhatIf</span></span>
<span data-ttu-id="3530b-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3530b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3530b-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3530b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3530b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3530b-122">CommonParameters</span></span>
<span data-ttu-id="3530b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3530b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3530b-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3530b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3530b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3530b-125">INPUTS</span></span>

### <span data-ttu-id="3530b-126">所有</span><span class="sxs-lookup"><span data-stu-id="3530b-126">None</span></span>
<span data-ttu-id="3530b-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3530b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3530b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3530b-128">OUTPUTS</span></span>

### <span data-ttu-id="3530b-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3530b-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="3530b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3530b-130">NOTES</span></span>

## <span data-ttu-id="3530b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3530b-131">RELATED LINKS</span></span>

[<span data-ttu-id="3530b-132">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3530b-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="3530b-133">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3530b-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="3530b-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3530b-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

