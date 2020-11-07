---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: 40c8229f1a14144516c465ef56908c3dd1fb9bc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788830"
---
# <span data-ttu-id="e85dc-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e85dc-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="e85dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e85dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e85dc-103">從指定的範圍中移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="e85dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="e85dc-104">SYNTAX</span></span>

### <span data-ttu-id="e85dc-105">RemoveTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="e85dc-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85dc-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="e85dc-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85dc-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="e85dc-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85dc-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="e85dc-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e85dc-109">說明</span><span class="sxs-lookup"><span data-stu-id="e85dc-109">DESCRIPTION</span></span>
<span data-ttu-id="e85dc-110">**AzApiManagementPolicy** Cmdlet 會從指定的範圍中移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="e85dc-111">示例</span><span class="sxs-lookup"><span data-stu-id="e85dc-111">EXAMPLES</span></span>

### <span data-ttu-id="e85dc-112">範例1：移除租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="e85dc-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="e85dc-113">這個命令會從 API 管理中移除租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="e85dc-114">範例2：移除產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="e85dc-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="e85dc-115">這個命令會從 API 管理中移除產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="e85dc-116">範例3：移除 API 作用中的原則</span><span class="sxs-lookup"><span data-stu-id="e85dc-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="e85dc-117">這個命令會從 API 管理中移除 API 作用中的原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="e85dc-118">範例4：移除操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="e85dc-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="e85dc-119">這個命令會從 API 管理移除操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="e85dc-120">參數</span><span class="sxs-lookup"><span data-stu-id="e85dc-120">PARAMETERS</span></span>

### <span data-ttu-id="e85dc-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e85dc-121">-ApiId</span></span>
<span data-ttu-id="e85dc-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e85dc-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="e85dc-123">如果您指定此參數，則 Cmdlet 會移除 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="e85dc-124">-內容</span><span class="sxs-lookup"><span data-stu-id="e85dc-124">-Context</span></span>
<span data-ttu-id="e85dc-125">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e85dc-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e85dc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85dc-126">-DefaultProfile</span></span>
<span data-ttu-id="e85dc-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e85dc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e85dc-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e85dc-128">-OperationId</span></span>
<span data-ttu-id="e85dc-129">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e85dc-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="e85dc-130">如果您使用 *ApiId* 參數指定此參數，這個 Cmdlet 會移除操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="e85dc-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e85dc-131">-PassThru</span></span>
<span data-ttu-id="e85dc-132">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="e85dc-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="e85dc-133">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="e85dc-133">-ProductId</span></span>
<span data-ttu-id="e85dc-134">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e85dc-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="e85dc-135">如果您指定此參數，則 Cmdlet 會移除產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="e85dc-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="e85dc-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e85dc-136">-Confirm</span></span>
<span data-ttu-id="e85dc-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e85dc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85dc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85dc-138">-WhatIf</span></span>
<span data-ttu-id="e85dc-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e85dc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85dc-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e85dc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85dc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85dc-141">CommonParameters</span></span>
<span data-ttu-id="e85dc-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e85dc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85dc-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e85dc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85dc-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e85dc-144">INPUTS</span></span>

### <span data-ttu-id="e85dc-145">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e85dc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e85dc-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e85dc-146">System.String</span></span>

### <span data-ttu-id="e85dc-147">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e85dc-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e85dc-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e85dc-148">OUTPUTS</span></span>

### <span data-ttu-id="e85dc-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e85dc-149">System.Boolean</span></span>

## <span data-ttu-id="e85dc-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e85dc-150">NOTES</span></span>

## <span data-ttu-id="e85dc-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e85dc-151">RELATED LINKS</span></span>

[<span data-ttu-id="e85dc-152">AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e85dc-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="e85dc-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e85dc-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


