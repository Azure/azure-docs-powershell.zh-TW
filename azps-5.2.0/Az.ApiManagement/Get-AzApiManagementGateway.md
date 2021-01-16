---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273652"
---
# <span data-ttu-id="37990-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="37990-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="37990-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37990-102">SYNOPSIS</span></span>
<span data-ttu-id="37990-103">取得全部或特定的 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="37990-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="37990-104">句法</span><span class="sxs-lookup"><span data-stu-id="37990-104">SYNTAX</span></span>

### <span data-ttu-id="37990-105">GetAllGateways (預設) </span><span class="sxs-lookup"><span data-stu-id="37990-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37990-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="37990-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37990-107">說明</span><span class="sxs-lookup"><span data-stu-id="37990-107">DESCRIPTION</span></span>
<span data-ttu-id="37990-108">**AzApiManagementGateway** Cmdlet 會取得全部或特定的 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="37990-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="37990-109">示例</span><span class="sxs-lookup"><span data-stu-id="37990-109">EXAMPLES</span></span>

### <span data-ttu-id="37990-110">範例1：取得所有閘道</span><span class="sxs-lookup"><span data-stu-id="37990-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="37990-111">這個命令會取得所有閘道。</span><span class="sxs-lookup"><span data-stu-id="37990-111">This command gets all gateways.</span></span>

### <span data-ttu-id="37990-112">範例2：依識別碼取得閘道</span><span class="sxs-lookup"><span data-stu-id="37990-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="37990-113">這個命令會取得閘道0123456789。</span><span class="sxs-lookup"><span data-stu-id="37990-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="37990-114">參數</span><span class="sxs-lookup"><span data-stu-id="37990-114">PARAMETERS</span></span>

### <span data-ttu-id="37990-115">-內容</span><span class="sxs-lookup"><span data-stu-id="37990-115">-Context</span></span>
<span data-ttu-id="37990-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="37990-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="37990-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="37990-117">This parameter is required.</span></span>

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

### <span data-ttu-id="37990-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37990-118">-DefaultProfile</span></span>
<span data-ttu-id="37990-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37990-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37990-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="37990-120">-GatewayId</span></span>
<span data-ttu-id="37990-121">閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37990-121">Identifier of a gateway.</span></span>
<span data-ttu-id="37990-122">如果已指定，將會嘗試依據識別碼尋找閘道。</span><span class="sxs-lookup"><span data-stu-id="37990-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="37990-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37990-123">CommonParameters</span></span>
<span data-ttu-id="37990-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37990-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37990-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37990-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37990-126">輸入</span><span class="sxs-lookup"><span data-stu-id="37990-126">INPUTS</span></span>

### <span data-ttu-id="37990-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="37990-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37990-128">System.object</span><span class="sxs-lookup"><span data-stu-id="37990-128">System.String</span></span>

## <span data-ttu-id="37990-129">輸出</span><span class="sxs-lookup"><span data-stu-id="37990-129">OUTPUTS</span></span>

### <span data-ttu-id="37990-130">ServiceManagement. PsApiManagementGateway （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="37990-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="37990-131">筆記</span><span class="sxs-lookup"><span data-stu-id="37990-131">NOTES</span></span>

## <span data-ttu-id="37990-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="37990-132">RELATED LINKS</span></span>
