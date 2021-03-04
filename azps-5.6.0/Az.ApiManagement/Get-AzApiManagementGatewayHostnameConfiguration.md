---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 27e833c526dea1b8df6451671ae2fd142c00b6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909254"
---
# <span data-ttu-id="e51a1-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51a1-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e51a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e51a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e51a1-103">為現有的閘道進行所有或特定的主機名稱組配置。</span><span class="sxs-lookup"><span data-stu-id="e51a1-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="e51a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="e51a1-104">SYNTAX</span></span>

### <span data-ttu-id="e51a1-105">GetByGatewayId (預設) </span><span class="sxs-lookup"><span data-stu-id="e51a1-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e51a1-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="e51a1-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e51a1-107">描述</span><span class="sxs-lookup"><span data-stu-id="e51a1-107">DESCRIPTION</span></span>
<span data-ttu-id="e51a1-108">**Get-AzApiManagementGatewayHostnameConfiguration** Cmdlet 會取得現有閘道的所有或特定主機名稱組。</span><span class="sxs-lookup"><span data-stu-id="e51a1-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="e51a1-109">例子</span><span class="sxs-lookup"><span data-stu-id="e51a1-109">EXAMPLES</span></span>

### <span data-ttu-id="e51a1-110">範例 1：取得閘道的所有主機名稱組</span><span class="sxs-lookup"><span data-stu-id="e51a1-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="e51a1-111">此命令會獲得「0123456789」閘道的所有主機名稱組。</span><span class="sxs-lookup"><span data-stu-id="e51a1-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="e51a1-112">範例 2：取得閘道的主機名稱組</span><span class="sxs-lookup"><span data-stu-id="e51a1-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="e51a1-113">此命令會針對「0123456789」閘道進行「123」主機名稱組配置。</span><span class="sxs-lookup"><span data-stu-id="e51a1-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="e51a1-114">參數</span><span class="sxs-lookup"><span data-stu-id="e51a1-114">PARAMETERS</span></span>

### <span data-ttu-id="e51a1-115">-內容</span><span class="sxs-lookup"><span data-stu-id="e51a1-115">-Context</span></span>
<span data-ttu-id="e51a1-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="e51a1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e51a1-117">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="e51a1-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51a1-118">-DefaultProfile</span></span>
<span data-ttu-id="e51a1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e51a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51a1-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e51a1-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="e51a1-121">Hostname Configuration 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e51a1-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="e51a1-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="e51a1-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51a1-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e51a1-123">-GatewayId</span></span>
<span data-ttu-id="e51a1-124">閘道識別碼。</span><span class="sxs-lookup"><span data-stu-id="e51a1-124">Gateway identifier.</span></span>
<span data-ttu-id="e51a1-125">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="e51a1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e51a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51a1-126">CommonParameters</span></span>
<span data-ttu-id="e51a1-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e51a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51a1-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e51a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51a1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e51a1-129">INPUTS</span></span>

### <span data-ttu-id="e51a1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="e51a1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e51a1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e51a1-131">System.String</span></span>

## <span data-ttu-id="e51a1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e51a1-132">OUTPUTS</span></span>

### <span data-ttu-id="e51a1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51a1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e51a1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e51a1-134">NOTES</span></span>

## <span data-ttu-id="e51a1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e51a1-135">RELATED LINKS</span></span>
