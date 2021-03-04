---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: b3bccc5d538c8ce5e3a79b621b48d75556ed0189
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909257"
---
# <span data-ttu-id="7369f-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7369f-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="7369f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7369f-102">SYNOPSIS</span></span>
<span data-ttu-id="7369f-103">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7369f-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="7369f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7369f-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7369f-105">描述</span><span class="sxs-lookup"><span data-stu-id="7369f-105">DESCRIPTION</span></span>
<span data-ttu-id="7369f-106">Cmdlet Get-AzEnvironment會獲得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7369f-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="7369f-107">例子</span><span class="sxs-lookup"><span data-stu-id="7369f-107">EXAMPLES</span></span>

### <span data-ttu-id="7369f-108">範例 1：取得 AzureCloud 環境</span><span class="sxs-lookup"><span data-stu-id="7369f-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="7369f-109">此範例顯示如何取得 AzureCloud (預設環境) 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7369f-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="7369f-110">範例 2：取得 AzureChinaCloud 環境</span><span class="sxs-lookup"><span data-stu-id="7369f-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="7369f-111">此範例顯示如何取得 AzureChinaCloud 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7369f-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="7369f-112">範例 3：取得 AzureUSGovernment 環境</span><span class="sxs-lookup"><span data-stu-id="7369f-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="7369f-113">此範例顯示如何取得 AzureUSGovernment 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7369f-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="7369f-114">參數</span><span class="sxs-lookup"><span data-stu-id="7369f-114">PARAMETERS</span></span>

### <span data-ttu-id="7369f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7369f-115">-DefaultProfile</span></span>
<span data-ttu-id="7369f-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7369f-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7369f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7369f-117">-Name</span></span>
<span data-ttu-id="7369f-118">指定要取得之 Azure 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7369f-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="7369f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7369f-119">CommonParameters</span></span>
<span data-ttu-id="7369f-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7369f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7369f-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7369f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7369f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7369f-122">INPUTS</span></span>

### <span data-ttu-id="7369f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7369f-123">System.String</span></span>

## <span data-ttu-id="7369f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7369f-124">OUTPUTS</span></span>

### <span data-ttu-id="7369f-125">Microsoft.Azure.Commands.Profile.models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7369f-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="7369f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7369f-126">NOTES</span></span>

## <span data-ttu-id="7369f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7369f-127">RELATED LINKS</span></span>

[<span data-ttu-id="7369f-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7369f-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="7369f-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7369f-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="7369f-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7369f-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

