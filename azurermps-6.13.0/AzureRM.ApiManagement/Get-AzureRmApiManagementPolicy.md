---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444171"
---
# <span data-ttu-id="9c21d-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9c21d-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="9c21d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c21d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c21d-103">取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c21d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c21d-104">SYNTAX</span></span>

### <span data-ttu-id="9c21d-105">GetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="9c21d-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c21d-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="9c21d-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c21d-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="9c21d-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c21d-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="9c21d-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c21d-109">說明</span><span class="sxs-lookup"><span data-stu-id="9c21d-109">DESCRIPTION</span></span>
<span data-ttu-id="9c21d-110">**AzureRmApiManagementPolicy** Cmdlet 會取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="9c21d-111">示例</span><span class="sxs-lookup"><span data-stu-id="9c21d-111">EXAMPLES</span></span>

### <span data-ttu-id="9c21d-112">範例1：取得租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="9c21d-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="9c21d-113">這個命令會取得租使用者層級原則，並將它儲存到名為 tenantpolicy.xml 的檔案。</span><span class="sxs-lookup"><span data-stu-id="9c21d-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="9c21d-114">範例2：取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="9c21d-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="9c21d-115">這個命令會取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="9c21d-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="9c21d-116">範例3：取得 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="9c21d-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="9c21d-117">這個命令會取得 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="9c21d-118">範例4：取得操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="9c21d-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="9c21d-119">這個命令會取得操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="9c21d-120">參數</span><span class="sxs-lookup"><span data-stu-id="9c21d-120">PARAMETERS</span></span>

### <span data-ttu-id="9c21d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9c21d-121">-ApiId</span></span>
<span data-ttu-id="9c21d-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c21d-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="9c21d-123">如果您指定此參數，則 Cmdlet 會傳回 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c21d-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9c21d-124">-ApiRevision</span></span>
<span data-ttu-id="9c21d-125">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c21d-125">Identifier of API Revision.</span></span> <span data-ttu-id="9c21d-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9c21d-126">This parameter is optional.</span></span> <span data-ttu-id="9c21d-127">如果未指定，將會從目前使用中的 api 修訂中檢索原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c21d-128">-內容</span><span class="sxs-lookup"><span data-stu-id="9c21d-128">-Context</span></span>
<span data-ttu-id="9c21d-129">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="9c21d-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="9c21d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c21d-130">-DefaultProfile</span></span>
<span data-ttu-id="9c21d-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c21d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c21d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9c21d-132">-Force</span></span>
<span data-ttu-id="9c21d-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="9c21d-133">ps_force</span></span>

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

### <span data-ttu-id="9c21d-134">-Format</span><span class="sxs-lookup"><span data-stu-id="9c21d-134">-Format</span></span>
<span data-ttu-id="9c21d-135">指定 API 管理原則的格式。</span><span class="sxs-lookup"><span data-stu-id="9c21d-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="9c21d-136">此參數的預設值為 "application/vnd. ms-azure-apim. policy + xml"。</span><span class="sxs-lookup"><span data-stu-id="9c21d-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="9c21d-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9c21d-137">-OperationId</span></span>
<span data-ttu-id="9c21d-138">指定現有 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c21d-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="9c21d-139">如果您使用 *ApiId* 指定此參數，則 Cmdlet 會傳回 operation 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c21d-140">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="9c21d-140">-ProductId</span></span>
<span data-ttu-id="9c21d-141">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c21d-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="9c21d-142">如果您指定此參數，則 Cmdlet 會傳回產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="9c21d-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c21d-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="9c21d-143">-SaveAs</span></span>
<span data-ttu-id="9c21d-144">指定要儲存結果的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="9c21d-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="9c21d-145">如果您沒有指定此參數，結果就會以流水線為 sting。</span><span class="sxs-lookup"><span data-stu-id="9c21d-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="9c21d-146">-確認</span><span class="sxs-lookup"><span data-stu-id="9c21d-146">-Confirm</span></span>
<span data-ttu-id="9c21d-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c21d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c21d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c21d-148">-WhatIf</span></span>
<span data-ttu-id="9c21d-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c21d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c21d-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c21d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c21d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c21d-151">CommonParameters</span></span>
<span data-ttu-id="9c21d-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c21d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c21d-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c21d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c21d-154">輸入</span><span class="sxs-lookup"><span data-stu-id="9c21d-154">INPUTS</span></span>

### <span data-ttu-id="9c21d-155">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9c21d-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9c21d-156">System.object</span><span class="sxs-lookup"><span data-stu-id="9c21d-156">System.String</span></span>

### <span data-ttu-id="9c21d-157">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9c21d-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c21d-158">輸出</span><span class="sxs-lookup"><span data-stu-id="9c21d-158">OUTPUTS</span></span>

### <span data-ttu-id="9c21d-159">System.object</span><span class="sxs-lookup"><span data-stu-id="9c21d-159">System.String</span></span>

## <span data-ttu-id="9c21d-160">筆記</span><span class="sxs-lookup"><span data-stu-id="9c21d-160">NOTES</span></span>

## <span data-ttu-id="9c21d-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c21d-161">RELATED LINKS</span></span>

[<span data-ttu-id="9c21d-162">移除-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9c21d-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="9c21d-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9c21d-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


