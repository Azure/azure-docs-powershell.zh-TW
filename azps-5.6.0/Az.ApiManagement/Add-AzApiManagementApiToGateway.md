---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 9c6d556845192a4bd6e5d6c856d113be4a4074a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907177"
---
# <span data-ttu-id="0e22f-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="0e22f-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="0e22f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e22f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e22f-103">將 API 附加到閘道。</span><span class="sxs-lookup"><span data-stu-id="0e22f-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="0e22f-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e22f-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e22f-105">描述</span><span class="sxs-lookup"><span data-stu-id="0e22f-105">DESCRIPTION</span></span>
<span data-ttu-id="0e22f-106">**Add-AzApiManagementApiToGateway** Cmdlet 會新增 Azure API 管理 API 至閘道。</span><span class="sxs-lookup"><span data-stu-id="0e22f-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="0e22f-107">例子</span><span class="sxs-lookup"><span data-stu-id="0e22f-107">EXAMPLES</span></span>

### <span data-ttu-id="0e22f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0e22f-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="0e22f-109">此命令會將指定的 API 新增到指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="0e22f-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="0e22f-110">參數</span><span class="sxs-lookup"><span data-stu-id="0e22f-110">PARAMETERS</span></span>

### <span data-ttu-id="0e22f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0e22f-111">-ApiId</span></span>
<span data-ttu-id="0e22f-112">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e22f-112">Identifier of existing API.</span></span>
<span data-ttu-id="0e22f-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="0e22f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0e22f-114">-內容</span><span class="sxs-lookup"><span data-stu-id="0e22f-114">-Context</span></span>
<span data-ttu-id="0e22f-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="0e22f-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0e22f-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="0e22f-116">This parameter is required.</span></span>

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

### <span data-ttu-id="0e22f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e22f-117">-DefaultProfile</span></span>
<span data-ttu-id="0e22f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e22f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e22f-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0e22f-119">-GatewayId</span></span>
<span data-ttu-id="0e22f-120">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e22f-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="0e22f-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="0e22f-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0e22f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e22f-122">-PassThru</span></span>
<span data-ttu-id="0e22f-123">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="0e22f-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0e22f-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="0e22f-124">This parameter is optional.</span></span>
<span data-ttu-id="0e22f-125">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="0e22f-125">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e22f-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="0e22f-126">-ProvisioningState</span></span>
<span data-ttu-id="0e22f-127">已建立 (的) 。</span><span class="sxs-lookup"><span data-stu-id="0e22f-127">Provisioning State (Created).</span></span>
<span data-ttu-id="0e22f-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="0e22f-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e22f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="0e22f-129">-Confirm</span></span>
<span data-ttu-id="0e22f-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0e22f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e22f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e22f-131">-WhatIf</span></span>
<span data-ttu-id="0e22f-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e22f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e22f-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e22f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e22f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e22f-134">CommonParameters</span></span>
<span data-ttu-id="0e22f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e22f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e22f-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e22f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e22f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="0e22f-137">INPUTS</span></span>

### <span data-ttu-id="0e22f-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="0e22f-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0e22f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0e22f-139">System.String</span></span>

### <span data-ttu-id="0e22f-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0e22f-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0e22f-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0e22f-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0e22f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0e22f-142">OUTPUTS</span></span>

### <span data-ttu-id="0e22f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e22f-143">System.Boolean</span></span>

## <span data-ttu-id="0e22f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0e22f-144">NOTES</span></span>

## <span data-ttu-id="0e22f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e22f-145">RELATED LINKS</span></span>

[<span data-ttu-id="0e22f-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="0e22f-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)