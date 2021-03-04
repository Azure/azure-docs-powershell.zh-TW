---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 980adceb2e5a76532c9b3175c015d5f4e3a6b2e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914201"
---
# <span data-ttu-id="07c5e-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="07c5e-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="07c5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="07c5e-103">獲得所有或特定的 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="07c5e-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="07c5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="07c5e-104">SYNTAX</span></span>

### <span data-ttu-id="07c5e-105">GetAllGateways (預設) </span><span class="sxs-lookup"><span data-stu-id="07c5e-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07c5e-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="07c5e-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c5e-107">描述</span><span class="sxs-lookup"><span data-stu-id="07c5e-107">DESCRIPTION</span></span>
<span data-ttu-id="07c5e-108">**Get-AzApiManagementGateway** Cmdlet 會取得所有或特定的 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="07c5e-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="07c5e-109">例子</span><span class="sxs-lookup"><span data-stu-id="07c5e-109">EXAMPLES</span></span>

### <span data-ttu-id="07c5e-110">範例 1：取得所有閘道</span><span class="sxs-lookup"><span data-stu-id="07c5e-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="07c5e-111">此命令會獲得所有閘道。</span><span class="sxs-lookup"><span data-stu-id="07c5e-111">This command gets all gateways.</span></span>

### <span data-ttu-id="07c5e-112">範例 2：以識別碼取得閘道</span><span class="sxs-lookup"><span data-stu-id="07c5e-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="07c5e-113">此命令會獲得閘道 0123456789。</span><span class="sxs-lookup"><span data-stu-id="07c5e-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="07c5e-114">參數</span><span class="sxs-lookup"><span data-stu-id="07c5e-114">PARAMETERS</span></span>

### <span data-ttu-id="07c5e-115">-內容</span><span class="sxs-lookup"><span data-stu-id="07c5e-115">-Context</span></span>
<span data-ttu-id="07c5e-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="07c5e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="07c5e-117">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="07c5e-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07c5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c5e-118">-DefaultProfile</span></span>
<span data-ttu-id="07c5e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07c5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07c5e-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="07c5e-120">-GatewayId</span></span>
<span data-ttu-id="07c5e-121">閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="07c5e-121">Identifier of a gateway.</span></span>
<span data-ttu-id="07c5e-122">如果指定，會嘗試根據識別碼尋找閘道。</span><span class="sxs-lookup"><span data-stu-id="07c5e-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07c5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c5e-123">CommonParameters</span></span>
<span data-ttu-id="07c5e-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07c5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c5e-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07c5e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c5e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="07c5e-126">INPUTS</span></span>

### <span data-ttu-id="07c5e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="07c5e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07c5e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="07c5e-128">System.String</span></span>

## <span data-ttu-id="07c5e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="07c5e-129">OUTPUTS</span></span>

### <span data-ttu-id="07c5e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="07c5e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="07c5e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="07c5e-131">NOTES</span></span>

## <span data-ttu-id="07c5e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="07c5e-132">RELATED LINKS</span></span>
