---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971307"
---
# <span data-ttu-id="cffb3-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cffb3-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="cffb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cffb3-102">SYNOPSIS</span></span>
<span data-ttu-id="cffb3-103">從指定的範圍中移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="cffb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="cffb3-104">SYNTAX</span></span>

### <span data-ttu-id="cffb3-105">RemoveTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="cffb3-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cffb3-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="cffb3-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cffb3-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="cffb3-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cffb3-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="cffb3-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cffb3-109">說明</span><span class="sxs-lookup"><span data-stu-id="cffb3-109">DESCRIPTION</span></span>
<span data-ttu-id="cffb3-110">**AzApiManagementPolicy** Cmdlet 會從指定的範圍中移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="cffb3-111">示例</span><span class="sxs-lookup"><span data-stu-id="cffb3-111">EXAMPLES</span></span>

### <span data-ttu-id="cffb3-112">範例1：移除租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="cffb3-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="cffb3-113">這個命令會從 API 管理中移除租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="cffb3-114">範例2：移除產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="cffb3-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="cffb3-115">這個命令會從 API 管理中移除產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="cffb3-116">範例3：移除 API 作用中的原則</span><span class="sxs-lookup"><span data-stu-id="cffb3-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="cffb3-117">這個命令會從 API 管理中移除 API 作用中的原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="cffb3-118">範例4：移除操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="cffb3-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="cffb3-119">這個命令會從 API 管理移除操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="cffb3-120">參數</span><span class="sxs-lookup"><span data-stu-id="cffb3-120">PARAMETERS</span></span>

### <span data-ttu-id="cffb3-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cffb3-121">-ApiId</span></span>
<span data-ttu-id="cffb3-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cffb3-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="cffb3-123">如果您指定此參數，則 Cmdlet 會移除 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="cffb3-124">-內容</span><span class="sxs-lookup"><span data-stu-id="cffb3-124">-Context</span></span>
<span data-ttu-id="cffb3-125">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="cffb3-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cffb3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffb3-126">-DefaultProfile</span></span>
<span data-ttu-id="cffb3-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cffb3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cffb3-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="cffb3-128">-OperationId</span></span>
<span data-ttu-id="cffb3-129">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cffb3-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="cffb3-130">如果您使用 *ApiId* 參數指定此參數，這個 Cmdlet 會移除操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="cffb3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cffb3-131">-PassThru</span></span>
<span data-ttu-id="cffb3-132">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="cffb3-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="cffb3-133">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="cffb3-133">-ProductId</span></span>
<span data-ttu-id="cffb3-134">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cffb3-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="cffb3-135">如果您指定此參數，則 Cmdlet 會移除產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="cffb3-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="cffb3-136">-確認</span><span class="sxs-lookup"><span data-stu-id="cffb3-136">-Confirm</span></span>
<span data-ttu-id="cffb3-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cffb3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cffb3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffb3-138">-WhatIf</span></span>
<span data-ttu-id="cffb3-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cffb3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cffb3-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cffb3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cffb3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffb3-141">CommonParameters</span></span>
<span data-ttu-id="cffb3-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cffb3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffb3-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cffb3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffb3-144">輸入</span><span class="sxs-lookup"><span data-stu-id="cffb3-144">INPUTS</span></span>

### <span data-ttu-id="cffb3-145">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cffb3-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cffb3-146">System.object</span><span class="sxs-lookup"><span data-stu-id="cffb3-146">System.String</span></span>

### <span data-ttu-id="cffb3-147">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="cffb3-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cffb3-148">輸出</span><span class="sxs-lookup"><span data-stu-id="cffb3-148">OUTPUTS</span></span>

### <span data-ttu-id="cffb3-149">System.object</span><span class="sxs-lookup"><span data-stu-id="cffb3-149">System.Boolean</span></span>

## <span data-ttu-id="cffb3-150">筆記</span><span class="sxs-lookup"><span data-stu-id="cffb3-150">NOTES</span></span>

## <span data-ttu-id="cffb3-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="cffb3-151">RELATED LINKS</span></span>

[<span data-ttu-id="cffb3-152">AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cffb3-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="cffb3-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cffb3-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


