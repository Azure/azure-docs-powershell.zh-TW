---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445199"
---
# <span data-ttu-id="8b165-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b165-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="8b165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b165-102">SYNOPSIS</span></span>
<span data-ttu-id="8b165-103">從指定的範圍中移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b165-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b165-104">SYNTAX</span></span>

### <span data-ttu-id="8b165-105">租使用者層級 (預設) </span><span class="sxs-lookup"><span data-stu-id="8b165-105">Tenant level (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b165-106">產品層級</span><span class="sxs-lookup"><span data-stu-id="8b165-106">Product level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b165-107">API 層級</span><span class="sxs-lookup"><span data-stu-id="8b165-107">API level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b165-108">操作層級</span><span class="sxs-lookup"><span data-stu-id="8b165-108">Operation level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b165-109">說明</span><span class="sxs-lookup"><span data-stu-id="8b165-109">DESCRIPTION</span></span>
<span data-ttu-id="8b165-110">**AzureRmApiManagementPolicy** Cmdlet 會從指定的範圍中移除 API 管理原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="8b165-111">示例</span><span class="sxs-lookup"><span data-stu-id="8b165-111">EXAMPLES</span></span>

### <span data-ttu-id="8b165-112">範例1：移除租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="8b165-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

<span data-ttu-id="8b165-113">這個命令會從 API 管理中移除租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="8b165-114">範例2：移除產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="8b165-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="8b165-115">這個命令會從 API 管理中移除產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="8b165-116">範例3：移除 API 作用中的原則</span><span class="sxs-lookup"><span data-stu-id="8b165-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="8b165-117">這個命令會從 API 管理中移除 API 作用中的原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="8b165-118">範例4：移除操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="8b165-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="8b165-119">這個命令會從 API 管理移除操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="8b165-120">參數</span><span class="sxs-lookup"><span data-stu-id="8b165-120">PARAMETERS</span></span>

### <span data-ttu-id="8b165-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8b165-121">-ApiId</span></span>
<span data-ttu-id="8b165-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b165-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="8b165-123">如果您指定此參數，則 Cmdlet 會移除 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b165-124">-內容</span><span class="sxs-lookup"><span data-stu-id="8b165-124">-Context</span></span>
<span data-ttu-id="8b165-125">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="8b165-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8b165-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8b165-126">-OperationId</span></span>
<span data-ttu-id="8b165-127">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b165-127">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="8b165-128">如果您使用 *ApiId* 參數指定此參數，這個 Cmdlet 會移除操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-128">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b165-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b165-129">-PassThru</span></span>
<span data-ttu-id="8b165-130">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="8b165-130">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="8b165-131">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="8b165-131">-ProductId</span></span>
<span data-ttu-id="8b165-132">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b165-132">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="8b165-133">如果您指定此參數，則 Cmdlet 會移除產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="8b165-133">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b165-134">-確認</span><span class="sxs-lookup"><span data-stu-id="8b165-134">-Confirm</span></span>
<span data-ttu-id="8b165-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b165-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b165-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b165-136">-WhatIf</span></span>
<span data-ttu-id="8b165-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b165-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b165-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b165-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b165-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b165-139">-DefaultProfile</span></span>
<span data-ttu-id="8b165-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b165-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b165-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b165-141">CommonParameters</span></span>
<span data-ttu-id="8b165-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b165-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b165-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b165-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b165-144">輸入</span><span class="sxs-lookup"><span data-stu-id="8b165-144">INPUTS</span></span>

## <span data-ttu-id="8b165-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8b165-145">OUTPUTS</span></span>

### <span data-ttu-id="8b165-146">布林值</span><span class="sxs-lookup"><span data-stu-id="8b165-146">Boolean</span></span>

## <span data-ttu-id="8b165-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8b165-147">NOTES</span></span>

## <span data-ttu-id="8b165-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b165-148">RELATED LINKS</span></span>

[<span data-ttu-id="8b165-149">AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b165-149">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="8b165-150">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b165-150">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


