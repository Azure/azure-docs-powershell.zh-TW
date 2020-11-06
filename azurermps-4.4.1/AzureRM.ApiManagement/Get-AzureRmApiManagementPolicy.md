---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450132"
---
# <span data-ttu-id="73389-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73389-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="73389-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73389-102">SYNOPSIS</span></span>
<span data-ttu-id="73389-103">取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="73389-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73389-104">句法</span><span class="sxs-lookup"><span data-stu-id="73389-104">SYNTAX</span></span>

### <span data-ttu-id="73389-105">租使用者層級 (預設) </span><span class="sxs-lookup"><span data-stu-id="73389-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73389-106">產品層級</span><span class="sxs-lookup"><span data-stu-id="73389-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73389-107">API 層級</span><span class="sxs-lookup"><span data-stu-id="73389-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73389-108">操作層級</span><span class="sxs-lookup"><span data-stu-id="73389-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73389-109">說明</span><span class="sxs-lookup"><span data-stu-id="73389-109">DESCRIPTION</span></span>
<span data-ttu-id="73389-110">**AzureRmApiManagementPolicy** Cmdlet 會取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="73389-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="73389-111">示例</span><span class="sxs-lookup"><span data-stu-id="73389-111">EXAMPLES</span></span>

### <span data-ttu-id="73389-112">範例1：取得租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="73389-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="73389-113">這個命令會取得租使用者層級原則，並將它儲存到名為 tenantpolicy.xml 的檔案。</span><span class="sxs-lookup"><span data-stu-id="73389-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="73389-114">範例2：取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="73389-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="73389-115">這個命令會取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="73389-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="73389-116">範例3：取得 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="73389-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="73389-117">這個命令會取得 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="73389-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="73389-118">範例4：取得操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="73389-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="73389-119">這個命令會取得操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="73389-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="73389-120">參數</span><span class="sxs-lookup"><span data-stu-id="73389-120">PARAMETERS</span></span>

### <span data-ttu-id="73389-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="73389-121">-ApiId</span></span>
<span data-ttu-id="73389-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73389-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="73389-123">如果您指定此參數，則 Cmdlet 會傳回 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="73389-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="73389-124">-內容</span><span class="sxs-lookup"><span data-stu-id="73389-124">-Context</span></span>
<span data-ttu-id="73389-125">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="73389-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="73389-126">-Force</span><span class="sxs-lookup"><span data-stu-id="73389-126">-Force</span></span>
<span data-ttu-id="73389-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="73389-127">ps_force</span></span>

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

### <span data-ttu-id="73389-128">-Format</span><span class="sxs-lookup"><span data-stu-id="73389-128">-Format</span></span>
<span data-ttu-id="73389-129">指定 API 管理原則的格式。</span><span class="sxs-lookup"><span data-stu-id="73389-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="73389-130">此參數的預設值為 "application/vnd. ms-azure-apim. policy + xml"。</span><span class="sxs-lookup"><span data-stu-id="73389-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="73389-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="73389-131">-OperationId</span></span>
<span data-ttu-id="73389-132">指定現有 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73389-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="73389-133">如果您使用 *ApiId* 指定此參數，則 Cmdlet 會傳回 operation 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="73389-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="73389-134">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="73389-134">-ProductId</span></span>
<span data-ttu-id="73389-135">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73389-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="73389-136">如果您指定此參數，則 Cmdlet 會傳回產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="73389-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="73389-137">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="73389-137">-SaveAs</span></span>
<span data-ttu-id="73389-138">指定要儲存結果的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="73389-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="73389-139">如果您沒有指定此參數，結果就會以流水線為 sting。</span><span class="sxs-lookup"><span data-stu-id="73389-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="73389-140">-確認</span><span class="sxs-lookup"><span data-stu-id="73389-140">-Confirm</span></span>
<span data-ttu-id="73389-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73389-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73389-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73389-142">-WhatIf</span></span>
<span data-ttu-id="73389-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73389-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73389-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73389-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73389-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73389-145">-DefaultProfile</span></span>
<span data-ttu-id="73389-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73389-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73389-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73389-147">CommonParameters</span></span>
<span data-ttu-id="73389-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73389-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73389-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73389-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73389-150">輸入</span><span class="sxs-lookup"><span data-stu-id="73389-150">INPUTS</span></span>

## <span data-ttu-id="73389-151">輸出</span><span class="sxs-lookup"><span data-stu-id="73389-151">OUTPUTS</span></span>

### <span data-ttu-id="73389-152">字串</span><span class="sxs-lookup"><span data-stu-id="73389-152">String</span></span>

## <span data-ttu-id="73389-153">筆記</span><span class="sxs-lookup"><span data-stu-id="73389-153">NOTES</span></span>

## <span data-ttu-id="73389-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="73389-154">RELATED LINKS</span></span>

[<span data-ttu-id="73389-155">移除-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73389-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="73389-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73389-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


