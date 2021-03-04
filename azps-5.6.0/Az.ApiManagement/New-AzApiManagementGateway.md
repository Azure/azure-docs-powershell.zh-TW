---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: 61a60949d88fd25c1205debb23aaed295122f376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903889"
---
# <span data-ttu-id="ac5b4-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ac5b4-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="ac5b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ac5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5b4-103">建立新閘道實體。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="ac5b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="ac5b4-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="ac5b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ac5b4-106">**New-AzApiManagementGateway** Cmdlet 會建立新的閘道實體。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="ac5b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="ac5b4-107">EXAMPLES</span></span>

### <span data-ttu-id="ac5b4-108">範例 1：建立閘道</span><span class="sxs-lookup"><span data-stu-id="ac5b4-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="ac5b4-109">此命令會建立閘道。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-109">This command creates a gateway.</span></span>

## <span data-ttu-id="ac5b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac5b4-110">PARAMETERS</span></span>

### <span data-ttu-id="ac5b4-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ac5b4-111">-Context</span></span>
<span data-ttu-id="ac5b4-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ac5b4-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ac5b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5b4-114">-DefaultProfile</span></span>
<span data-ttu-id="ac5b4-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5b4-116">-描述</span><span class="sxs-lookup"><span data-stu-id="ac5b4-116">-Description</span></span>
<span data-ttu-id="ac5b4-117">閘道描述。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-117">Gateway description.</span></span>
<span data-ttu-id="ac5b4-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5b4-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ac5b4-119">-GatewayId</span></span>
<span data-ttu-id="ac5b4-120">新閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-120">Identifier of new gateway.</span></span>
<span data-ttu-id="ac5b4-121">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-121">This parameter is optional.</span></span>
<span data-ttu-id="ac5b4-122">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-122">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5b4-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="ac5b4-123">-LocationData</span></span>
<span data-ttu-id="ac5b4-124">閘道位置。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-124">Gateway location.</span></span>
<span data-ttu-id="ac5b4-125">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5b4-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ac5b4-126">-Confirm</span></span>
<span data-ttu-id="ac5b4-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac5b4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5b4-128">-WhatIf</span></span>
<span data-ttu-id="ac5b4-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac5b4-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac5b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5b4-131">CommonParameters</span></span>
<span data-ttu-id="ac5b4-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ac5b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5b4-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac5b4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5b4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ac5b4-134">INPUTS</span></span>

### <span data-ttu-id="ac5b4-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac5b4-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac5b4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ac5b4-136">System.String</span></span>

### <span data-ttu-id="ac5b4-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="ac5b4-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="ac5b4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ac5b4-138">OUTPUTS</span></span>

### <span data-ttu-id="ac5b4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ac5b4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="ac5b4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ac5b4-140">NOTES</span></span>

## <span data-ttu-id="ac5b4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac5b4-141">RELATED LINKS</span></span>
