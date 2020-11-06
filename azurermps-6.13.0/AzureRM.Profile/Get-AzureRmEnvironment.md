---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448977"
---
# <span data-ttu-id="e0901-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0901-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="e0901-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0901-102">SYNOPSIS</span></span>
<span data-ttu-id="e0901-103">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e0901-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0901-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0901-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0901-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0901-105">DESCRIPTION</span></span>
<span data-ttu-id="e0901-106">Get-AzureRmEnvironment Cmdlet 會取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e0901-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="e0901-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0901-107">EXAMPLES</span></span>

### <span data-ttu-id="e0901-108">範例1：取得 AzureCloud 環境</span><span class="sxs-lookup"><span data-stu-id="e0901-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="e0901-109">這個範例示範如何取得 AzureCloud (預設) 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e0901-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="e0901-110">範例2：取得 AzureChinaCloud 環境</span><span class="sxs-lookup"><span data-stu-id="e0901-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="e0901-111">此範例說明如何取得 AzureChinaCloud 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e0901-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="e0901-112">範例3：取得 AzureUSGovernment 環境</span><span class="sxs-lookup"><span data-stu-id="e0901-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="e0901-113">此範例說明如何取得 AzureUSGovernment 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e0901-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="e0901-114">參數</span><span class="sxs-lookup"><span data-stu-id="e0901-114">PARAMETERS</span></span>

### <span data-ttu-id="e0901-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0901-115">-DefaultProfile</span></span>
<span data-ttu-id="e0901-116">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0901-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0901-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0901-117">-Name</span></span>
<span data-ttu-id="e0901-118">指定要取得的 Azure 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="e0901-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0901-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0901-119">CommonParameters</span></span>
<span data-ttu-id="e0901-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0901-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0901-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0901-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0901-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e0901-122">INPUTS</span></span>

### <span data-ttu-id="e0901-123">System.object</span><span class="sxs-lookup"><span data-stu-id="e0901-123">System.String</span></span>

## <span data-ttu-id="e0901-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e0901-124">OUTPUTS</span></span>

### <span data-ttu-id="e0901-125">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="e0901-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e0901-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e0901-126">NOTES</span></span>

## <span data-ttu-id="e0901-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0901-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0901-128">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0901-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="e0901-129">移除-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0901-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="e0901-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0901-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

