---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448807"
---
# <span data-ttu-id="42838-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42838-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="42838-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42838-102">SYNOPSIS</span></span>
<span data-ttu-id="42838-103">取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="42838-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42838-104">句法</span><span class="sxs-lookup"><span data-stu-id="42838-104">SYNTAX</span></span>

### <span data-ttu-id="42838-105">GetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="42838-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42838-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="42838-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42838-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="42838-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42838-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="42838-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42838-109">說明</span><span class="sxs-lookup"><span data-stu-id="42838-109">DESCRIPTION</span></span>
<span data-ttu-id="42838-110">**AzureRmApiManagementPolicy** Cmdlet 會取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="42838-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="42838-111">示例</span><span class="sxs-lookup"><span data-stu-id="42838-111">EXAMPLES</span></span>

### <span data-ttu-id="42838-112">範例1：取得租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="42838-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="42838-113">這個命令會取得租使用者層級原則，並將它儲存到名為 tenantpolicy.xml 的檔案。</span><span class="sxs-lookup"><span data-stu-id="42838-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="42838-114">範例2：取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="42838-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="42838-115">這個命令會取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="42838-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="42838-116">範例3：取得 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="42838-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="42838-117">這個命令會取得 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="42838-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="42838-118">範例4：取得操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="42838-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="42838-119">這個命令會取得操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="42838-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="42838-120">參數</span><span class="sxs-lookup"><span data-stu-id="42838-120">PARAMETERS</span></span>

### <span data-ttu-id="42838-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="42838-121">-ApiId</span></span>
<span data-ttu-id="42838-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="42838-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="42838-123">如果您指定此參數，則 Cmdlet 會傳回 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="42838-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-124">-內容</span><span class="sxs-lookup"><span data-stu-id="42838-124">-Context</span></span>
<span data-ttu-id="42838-125">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="42838-125">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42838-126">-DefaultProfile</span></span>
<span data-ttu-id="42838-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42838-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42838-128">-Force</span><span class="sxs-lookup"><span data-stu-id="42838-128">-Force</span></span>
<span data-ttu-id="42838-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="42838-129">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-130">-Format</span><span class="sxs-lookup"><span data-stu-id="42838-130">-Format</span></span>
<span data-ttu-id="42838-131">指定 API 管理原則的格式。</span><span class="sxs-lookup"><span data-stu-id="42838-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="42838-132">此參數的預設值為 "application/vnd. ms-azure-apim. policy + xml"。</span><span class="sxs-lookup"><span data-stu-id="42838-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-133">-OperationId</span><span class="sxs-lookup"><span data-stu-id="42838-133">-OperationId</span></span>
<span data-ttu-id="42838-134">指定現有 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="42838-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="42838-135">如果您使用 *ApiId* 指定此參數，則 Cmdlet 會傳回 operation 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="42838-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-136">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="42838-136">-ProductId</span></span>
<span data-ttu-id="42838-137">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="42838-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="42838-138">如果您指定此參數，則 Cmdlet 會傳回產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="42838-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-139">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="42838-139">-SaveAs</span></span>
<span data-ttu-id="42838-140">指定要儲存結果的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="42838-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="42838-141">如果您沒有指定此參數，結果就會以流水線為 sting。</span><span class="sxs-lookup"><span data-stu-id="42838-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42838-142">-確認</span><span class="sxs-lookup"><span data-stu-id="42838-142">-Confirm</span></span>
<span data-ttu-id="42838-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42838-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42838-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42838-144">-WhatIf</span></span>
<span data-ttu-id="42838-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42838-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42838-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42838-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42838-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42838-147">CommonParameters</span></span>
<span data-ttu-id="42838-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42838-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42838-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42838-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42838-150">輸入</span><span class="sxs-lookup"><span data-stu-id="42838-150">INPUTS</span></span>

### <span data-ttu-id="42838-151">所有</span><span class="sxs-lookup"><span data-stu-id="42838-151">None</span></span>
<span data-ttu-id="42838-152">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="42838-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42838-153">輸出</span><span class="sxs-lookup"><span data-stu-id="42838-153">OUTPUTS</span></span>

### <span data-ttu-id="42838-154">字串</span><span class="sxs-lookup"><span data-stu-id="42838-154">String</span></span>

## <span data-ttu-id="42838-155">筆記</span><span class="sxs-lookup"><span data-stu-id="42838-155">NOTES</span></span>

## <span data-ttu-id="42838-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="42838-156">RELATED LINKS</span></span>

[<span data-ttu-id="42838-157">移除-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42838-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="42838-158">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42838-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


