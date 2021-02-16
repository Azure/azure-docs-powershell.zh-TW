---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398133"
---
# <span data-ttu-id="62724-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="62724-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="62724-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62724-102">SYNOPSIS</span></span>
<span data-ttu-id="62724-103">建立物件 `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="62724-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="62724-104">語法</span><span class="sxs-lookup"><span data-stu-id="62724-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62724-105">描述</span><span class="sxs-lookup"><span data-stu-id="62724-105">DESCRIPTION</span></span>

<span data-ttu-id="62724-106">**New-AzApiManagementBackendServiceFabric** Cmdlet 會建立要用於 `PsApiManagementServiceFabric` Cmdlet **New-AzApiManagementBackend** 和 **Set-AzApiManagementBackend** 的物件。</span><span class="sxs-lookup"><span data-stu-id="62724-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="62724-107">例子</span><span class="sxs-lookup"><span data-stu-id="62724-107">EXAMPLES</span></span>

### <span data-ttu-id="62724-108">範例 1：建立後端服務結構In-Memory物件</span><span class="sxs-lookup"><span data-stu-id="62724-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="62724-109">建立後端服務結構合約</span><span class="sxs-lookup"><span data-stu-id="62724-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="62724-110">參數</span><span class="sxs-lookup"><span data-stu-id="62724-110">PARAMETERS</span></span>

### <span data-ttu-id="62724-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="62724-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="62724-112">管理端點的用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="62724-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="62724-113">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="62724-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62724-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62724-114">-DefaultProfile</span></span>
<span data-ttu-id="62724-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62724-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62724-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="62724-116">-ManagementEndpoint</span></span>
<span data-ttu-id="62724-117">服務結構組群管理端點。</span><span class="sxs-lookup"><span data-stu-id="62724-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="62724-118">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="62724-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62724-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="62724-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="62724-120">解決 Service Fabric 分割時重試次數上限。</span><span class="sxs-lookup"><span data-stu-id="62724-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="62724-121">此參數為選擇性，預設值為 5。</span><span class="sxs-lookup"><span data-stu-id="62724-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62724-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="62724-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="62724-123">憑證組管理服務用於 tls 通訊的指紋。此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="62724-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62724-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="62724-124">-ServerX509Name</span></span>
<span data-ttu-id="62724-125">Server X509 憑證名稱集合。</span><span class="sxs-lookup"><span data-stu-id="62724-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="62724-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="62724-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62724-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62724-127">CommonParameters</span></span>
<span data-ttu-id="62724-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62724-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62724-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62724-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62724-130">輸入</span><span class="sxs-lookup"><span data-stu-id="62724-130">INPUTS</span></span>

### <span data-ttu-id="62724-131">System.String</span><span class="sxs-lookup"><span data-stu-id="62724-131">System.String</span></span>

## <span data-ttu-id="62724-132">輸出</span><span class="sxs-lookup"><span data-stu-id="62724-132">OUTPUTS</span></span>

### <span data-ttu-id="62724-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="62724-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="62724-134">筆記</span><span class="sxs-lookup"><span data-stu-id="62724-134">NOTES</span></span>

## <span data-ttu-id="62724-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="62724-135">RELATED LINKS</span></span>

[<span data-ttu-id="62724-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62724-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="62724-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62724-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="62724-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="62724-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="62724-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62724-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="62724-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62724-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
