---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: aecf4982b6a48ac5afca1379e1f920cfa3d6e267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908681"
---
# <span data-ttu-id="37676-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37676-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="37676-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37676-102">SYNOPSIS</span></span>
<span data-ttu-id="37676-103">從指定的範圍移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="37676-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="37676-104">語法</span><span class="sxs-lookup"><span data-stu-id="37676-104">SYNTAX</span></span>

### <span data-ttu-id="37676-105">RemoveTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="37676-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37676-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="37676-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37676-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="37676-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37676-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="37676-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37676-109">描述</span><span class="sxs-lookup"><span data-stu-id="37676-109">DESCRIPTION</span></span>
<span data-ttu-id="37676-110">**Remove-AzApiManagementPolidlet** 會從指定的範圍移除 API 管理政策。</span><span class="sxs-lookup"><span data-stu-id="37676-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="37676-111">例子</span><span class="sxs-lookup"><span data-stu-id="37676-111">EXAMPLES</span></span>

### <span data-ttu-id="37676-112">範例 1：移除租使用者層級策略</span><span class="sxs-lookup"><span data-stu-id="37676-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="37676-113">此命令會從 API 管理移除租使用者層級策略。</span><span class="sxs-lookup"><span data-stu-id="37676-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="37676-114">範例 2：移除產品範圍策略</span><span class="sxs-lookup"><span data-stu-id="37676-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="37676-115">此命令會從 API 管理移除產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="37676-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="37676-116">範例 3：移除 API 範圍策略</span><span class="sxs-lookup"><span data-stu-id="37676-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="37676-117">此命令會從 API 管理移除 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="37676-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="37676-118">範例 4：移除作業範圍策略</span><span class="sxs-lookup"><span data-stu-id="37676-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="37676-119">此命令會從 API 管理移除作業範圍策略。</span><span class="sxs-lookup"><span data-stu-id="37676-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="37676-120">參數</span><span class="sxs-lookup"><span data-stu-id="37676-120">PARAMETERS</span></span>

### <span data-ttu-id="37676-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="37676-121">-ApiId</span></span>
<span data-ttu-id="37676-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37676-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="37676-123">如果您指定此參數，Cmdlet 會移除 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="37676-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37676-124">-內容</span><span class="sxs-lookup"><span data-stu-id="37676-124">-Context</span></span>
<span data-ttu-id="37676-125">指定 **PsApiManagementCoNtext 物件** 的實例。</span><span class="sxs-lookup"><span data-stu-id="37676-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="37676-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37676-126">-DefaultProfile</span></span>
<span data-ttu-id="37676-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37676-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37676-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="37676-128">-OperationId</span></span>
<span data-ttu-id="37676-129">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37676-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="37676-130">如果您使用 *ApiId* 參數指定此參數，此 Cmdlet 會移除作業範圍策略。</span><span class="sxs-lookup"><span data-stu-id="37676-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37676-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37676-131">-PassThru</span></span>
<span data-ttu-id="37676-132">表示此 Cmdlet 會$True值 ，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="37676-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="37676-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="37676-133">-ProductId</span></span>
<span data-ttu-id="37676-134">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37676-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="37676-135">如果您指定此參數，Cmdlet 會移除產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="37676-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37676-136">-確認</span><span class="sxs-lookup"><span data-stu-id="37676-136">-Confirm</span></span>
<span data-ttu-id="37676-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37676-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37676-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37676-138">-WhatIf</span></span>
<span data-ttu-id="37676-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37676-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37676-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37676-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37676-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37676-141">CommonParameters</span></span>
<span data-ttu-id="37676-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37676-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37676-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37676-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37676-144">輸入</span><span class="sxs-lookup"><span data-stu-id="37676-144">INPUTS</span></span>

### <span data-ttu-id="37676-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="37676-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37676-146">System.String</span><span class="sxs-lookup"><span data-stu-id="37676-146">System.String</span></span>

### <span data-ttu-id="37676-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37676-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37676-148">輸出</span><span class="sxs-lookup"><span data-stu-id="37676-148">OUTPUTS</span></span>

### <span data-ttu-id="37676-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37676-149">System.Boolean</span></span>

## <span data-ttu-id="37676-150">筆記</span><span class="sxs-lookup"><span data-stu-id="37676-150">NOTES</span></span>

## <span data-ttu-id="37676-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="37676-151">RELATED LINKS</span></span>

[<span data-ttu-id="37676-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37676-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="37676-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37676-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


