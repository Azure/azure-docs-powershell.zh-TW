---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141173"
---
# <span data-ttu-id="edfa4-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="edfa4-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="edfa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edfa4-102">SYNOPSIS</span></span>
<span data-ttu-id="edfa4-103">將 API 附加到閘道。</span><span class="sxs-lookup"><span data-stu-id="edfa4-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="edfa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="edfa4-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfa4-105">說明</span><span class="sxs-lookup"><span data-stu-id="edfa4-105">DESCRIPTION</span></span>
<span data-ttu-id="edfa4-106">**AzApiManagementApiFromGateway** Cmdlet 會將 API 附加至閘道。</span><span class="sxs-lookup"><span data-stu-id="edfa4-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="edfa4-107">示例</span><span class="sxs-lookup"><span data-stu-id="edfa4-107">EXAMPLES</span></span>

### <span data-ttu-id="edfa4-108">範例1：從閘道移除 API</span><span class="sxs-lookup"><span data-stu-id="edfa4-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="edfa4-109">這個命令會從閘道中移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="edfa4-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="edfa4-110">參數</span><span class="sxs-lookup"><span data-stu-id="edfa4-110">PARAMETERS</span></span>

### <span data-ttu-id="edfa4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="edfa4-111">-ApiId</span></span>
<span data-ttu-id="edfa4-112">要從閘道中移除之現有 Api 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="edfa4-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="edfa4-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="edfa4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="edfa4-114">-內容</span><span class="sxs-lookup"><span data-stu-id="edfa4-114">-Context</span></span>
<span data-ttu-id="edfa4-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="edfa4-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="edfa4-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="edfa4-116">This parameter is required.</span></span>

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

### <span data-ttu-id="edfa4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfa4-117">-DefaultProfile</span></span>
<span data-ttu-id="edfa4-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edfa4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edfa4-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="edfa4-119">-GatewayId</span></span>
<span data-ttu-id="edfa4-120">要從中移除 API 之現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="edfa4-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="edfa4-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="edfa4-121">This parameter is required.</span></span>

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

### <span data-ttu-id="edfa4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edfa4-122">-PassThru</span></span>
<span data-ttu-id="edfa4-123">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="edfa4-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="edfa4-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="edfa4-124">This parameter is optional.</span></span>
<span data-ttu-id="edfa4-125">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="edfa4-125">Default value is false.</span></span>

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

### <span data-ttu-id="edfa4-126">-確認</span><span class="sxs-lookup"><span data-stu-id="edfa4-126">-Confirm</span></span>
<span data-ttu-id="edfa4-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="edfa4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfa4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfa4-128">-WhatIf</span></span>
<span data-ttu-id="edfa4-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edfa4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edfa4-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edfa4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfa4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfa4-131">CommonParameters</span></span>
<span data-ttu-id="edfa4-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edfa4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfa4-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="edfa4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfa4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="edfa4-134">INPUTS</span></span>

### <span data-ttu-id="edfa4-135">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="edfa4-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="edfa4-136">System.object</span><span class="sxs-lookup"><span data-stu-id="edfa4-136">System.String</span></span>

### <span data-ttu-id="edfa4-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="edfa4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="edfa4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="edfa4-138">OUTPUTS</span></span>

### <span data-ttu-id="edfa4-139">System.object</span><span class="sxs-lookup"><span data-stu-id="edfa4-139">System.Boolean</span></span>

## <span data-ttu-id="edfa4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="edfa4-140">NOTES</span></span>

## <span data-ttu-id="edfa4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="edfa4-141">RELATED LINKS</span></span>
