---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141775"
---
# <span data-ttu-id="9d9f9-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="9d9f9-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="9d9f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9f9-103">將 API 附加到閘道。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="9d9f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d9f9-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d9f9-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9f9-106">**AzApiManagementApiToGateway** Cmdlet 會將 Azure API 管理 API 新增至閘道。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="9d9f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d9f9-107">EXAMPLES</span></span>

### <span data-ttu-id="9d9f9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9d9f9-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="9d9f9-109">這個命令會將指定的 API 新增至指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="9d9f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d9f9-110">PARAMETERS</span></span>

### <span data-ttu-id="9d9f9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9d9f9-111">-ApiId</span></span>
<span data-ttu-id="9d9f9-112">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-112">Identifier of existing API.</span></span>
<span data-ttu-id="9d9f9-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9d9f9-114">-內容</span><span class="sxs-lookup"><span data-stu-id="9d9f9-114">-Context</span></span>
<span data-ttu-id="9d9f9-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9d9f9-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9d9f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9f9-117">-DefaultProfile</span></span>
<span data-ttu-id="9d9f9-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9f9-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9d9f9-119">-GatewayId</span></span>
<span data-ttu-id="9d9f9-120">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="9d9f9-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-121">This parameter is required.</span></span>

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

### <span data-ttu-id="9d9f9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d9f9-122">-PassThru</span></span>
<span data-ttu-id="9d9f9-123">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9d9f9-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-124">This parameter is optional.</span></span>
<span data-ttu-id="9d9f9-125">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-125">Default value is false.</span></span>

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

### <span data-ttu-id="9d9f9-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="9d9f9-126">-ProvisioningState</span></span>
<span data-ttu-id="9d9f9-127">已建立 () 的 [提供狀態]。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-127">Provisioning State (Created).</span></span>
<span data-ttu-id="9d9f9-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d9f9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9d9f9-129">-Confirm</span></span>
<span data-ttu-id="9d9f9-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9f9-131">-WhatIf</span></span>
<span data-ttu-id="9d9f9-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d9f9-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9f9-134">CommonParameters</span></span>
<span data-ttu-id="9d9f9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9f9-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d9f9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9f9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9d9f9-137">INPUTS</span></span>

### <span data-ttu-id="9d9f9-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9d9f9-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9d9f9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9d9f9-139">System.String</span></span>

### <span data-ttu-id="9d9f9-140">ApiManagement 為 Nullable "1 [PsApiManagementGatewayApiProvisioningState，，ServiceManagement，Version = ServiceManagement，Culture = 中立，PublicKeyToken = null]]。）），）的區域性 = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9d9f9-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9d9f9-141">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9d9f9-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9d9f9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9d9f9-142">OUTPUTS</span></span>

### <span data-ttu-id="9d9f9-143">System.object</span><span class="sxs-lookup"><span data-stu-id="9d9f9-143">System.Boolean</span></span>

## <span data-ttu-id="9d9f9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9d9f9-144">NOTES</span></span>

## <span data-ttu-id="9d9f9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d9f9-145">RELATED LINKS</span></span>

[<span data-ttu-id="9d9f9-146">移除-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="9d9f9-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)