---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137741"
---
# <span data-ttu-id="f0ecb-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0ecb-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="f0ecb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ecb-103">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="f0ecb-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0ecb-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0ecb-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ecb-106">Get-AzEnvironment Cmdlet 會取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="f0ecb-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ecb-108">範例1：取得 AzureCloud 環境</span><span class="sxs-lookup"><span data-stu-id="f0ecb-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="f0ecb-109">這個範例示範如何取得 AzureCloud (預設) 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="f0ecb-110">範例2：取得 AzureChinaCloud 環境</span><span class="sxs-lookup"><span data-stu-id="f0ecb-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="f0ecb-111">此範例說明如何取得 AzureChinaCloud 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="f0ecb-112">範例3：取得 AzureUSGovernment 環境</span><span class="sxs-lookup"><span data-stu-id="f0ecb-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="f0ecb-113">此範例說明如何取得 AzureUSGovernment 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="f0ecb-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0ecb-114">PARAMETERS</span></span>

### <span data-ttu-id="f0ecb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ecb-115">-DefaultProfile</span></span>
<span data-ttu-id="f0ecb-116">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0ecb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0ecb-117">-Name</span></span>
<span data-ttu-id="f0ecb-118">指定要取得的 Azure 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="f0ecb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ecb-119">CommonParameters</span></span>
<span data-ttu-id="f0ecb-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ecb-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ecb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f0ecb-122">INPUTS</span></span>

### <span data-ttu-id="f0ecb-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f0ecb-123">System.String</span></span>

## <span data-ttu-id="f0ecb-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f0ecb-124">OUTPUTS</span></span>

### <span data-ttu-id="f0ecb-125">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f0ecb-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f0ecb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f0ecb-126">NOTES</span></span>

## <span data-ttu-id="f0ecb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0ecb-127">RELATED LINKS</span></span>

[<span data-ttu-id="f0ecb-128">附加 AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0ecb-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="f0ecb-129">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0ecb-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="f0ecb-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0ecb-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

