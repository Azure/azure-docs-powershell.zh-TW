---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134258"
---
# <span data-ttu-id="11391-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="11391-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="11391-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11391-102">SYNOPSIS</span></span>
<span data-ttu-id="11391-103">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="11391-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="11391-104">句法</span><span class="sxs-lookup"><span data-stu-id="11391-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11391-105">說明</span><span class="sxs-lookup"><span data-stu-id="11391-105">DESCRIPTION</span></span>
<span data-ttu-id="11391-106">Get-AzEnvironment Cmdlet 會取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="11391-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="11391-107">示例</span><span class="sxs-lookup"><span data-stu-id="11391-107">EXAMPLES</span></span>

### <span data-ttu-id="11391-108">範例1：取得 AzureCloud 環境</span><span class="sxs-lookup"><span data-stu-id="11391-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="11391-109">這個範例示範如何取得 AzureCloud (預設) 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="11391-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="11391-110">範例2：取得 AzureChinaCloud 環境</span><span class="sxs-lookup"><span data-stu-id="11391-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="11391-111">此範例說明如何取得 AzureChinaCloud 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="11391-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="11391-112">範例3：取得 AzureUSGovernment 環境</span><span class="sxs-lookup"><span data-stu-id="11391-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="11391-113">此範例說明如何取得 AzureUSGovernment 環境的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="11391-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="11391-114">參數</span><span class="sxs-lookup"><span data-stu-id="11391-114">PARAMETERS</span></span>

### <span data-ttu-id="11391-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11391-115">-DefaultProfile</span></span>
<span data-ttu-id="11391-116">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="11391-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11391-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="11391-117">-Name</span></span>
<span data-ttu-id="11391-118">指定要取得的 Azure 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="11391-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="11391-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11391-119">CommonParameters</span></span>
<span data-ttu-id="11391-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11391-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11391-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11391-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11391-122">輸入</span><span class="sxs-lookup"><span data-stu-id="11391-122">INPUTS</span></span>

### <span data-ttu-id="11391-123">System.object</span><span class="sxs-lookup"><span data-stu-id="11391-123">System.String</span></span>

## <span data-ttu-id="11391-124">輸出</span><span class="sxs-lookup"><span data-stu-id="11391-124">OUTPUTS</span></span>

### <span data-ttu-id="11391-125">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="11391-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="11391-126">筆記</span><span class="sxs-lookup"><span data-stu-id="11391-126">NOTES</span></span>

## <span data-ttu-id="11391-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="11391-127">RELATED LINKS</span></span>

[<span data-ttu-id="11391-128">附加 AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="11391-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="11391-129">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="11391-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="11391-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="11391-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

