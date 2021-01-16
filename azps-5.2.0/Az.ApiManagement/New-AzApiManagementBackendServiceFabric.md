---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275875"
---
# <span data-ttu-id="ae489-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ae489-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="ae489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae489-102">SYNOPSIS</span></span>
<span data-ttu-id="ae489-103">建立物件 `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="ae489-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="ae489-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae489-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae489-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae489-105">DESCRIPTION</span></span>

<span data-ttu-id="ae489-106">**新的-AzApiManagementBackendServiceFabric** Cmdlet `PsApiManagementServiceFabric` 會建立要在 Cmdlet **New-AzApiManagementBackend** 和 **Set AzApiManagementBackend** 中使用的物件。</span><span class="sxs-lookup"><span data-stu-id="ae489-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="ae489-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae489-107">EXAMPLES</span></span>

### <span data-ttu-id="ae489-108">範例1：建立後端服務結構 In-Memory 物件</span><span class="sxs-lookup"><span data-stu-id="ae489-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="ae489-109">建立後端服務結構合約</span><span class="sxs-lookup"><span data-stu-id="ae489-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="ae489-110">參數</span><span class="sxs-lookup"><span data-stu-id="ae489-110">PARAMETERS</span></span>

### <span data-ttu-id="ae489-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ae489-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="ae489-112">管理端點的用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="ae489-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="ae489-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ae489-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ae489-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae489-114">-DefaultProfile</span></span>
<span data-ttu-id="ae489-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae489-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae489-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae489-116">-ManagementEndpoint</span></span>
<span data-ttu-id="ae489-117">Service Fabric 群集管理端點。</span><span class="sxs-lookup"><span data-stu-id="ae489-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="ae489-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ae489-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ae489-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="ae489-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="ae489-120">解析 Service Fabric 分區時的最大重試次數。</span><span class="sxs-lookup"><span data-stu-id="ae489-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="ae489-121">此參數為 optional，且預設值為5。</span><span class="sxs-lookup"><span data-stu-id="ae489-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="ae489-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ae489-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="ae489-123">[憑證群集管理服務] 用來進行 tls 通訊的指紋。這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ae489-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="ae489-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="ae489-124">-ServerX509Name</span></span>
<span data-ttu-id="ae489-125">Server X509 憑證名稱集合。</span><span class="sxs-lookup"><span data-stu-id="ae489-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="ae489-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ae489-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="ae489-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae489-127">CommonParameters</span></span>
<span data-ttu-id="ae489-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae489-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae489-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae489-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae489-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ae489-130">INPUTS</span></span>

### <span data-ttu-id="ae489-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ae489-131">System.String</span></span>

## <span data-ttu-id="ae489-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ae489-132">OUTPUTS</span></span>

### <span data-ttu-id="ae489-133">ServiceManagement. PsApiManagementServiceFabric （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ae489-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="ae489-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ae489-134">NOTES</span></span>

## <span data-ttu-id="ae489-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae489-135">RELATED LINKS</span></span>

[<span data-ttu-id="ae489-136">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ae489-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="ae489-137">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ae489-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ae489-138">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ae489-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ae489-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ae489-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ae489-140">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ae489-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
