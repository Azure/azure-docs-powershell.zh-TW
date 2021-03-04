---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 3858d24bb0c714da0e48ad5834870ec5127eb5e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905258"
---
# <span data-ttu-id="546e2-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="546e2-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="546e2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="546e2-102">SYNOPSIS</span></span>
<span data-ttu-id="546e2-103">設定 API 管理的指定範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="546e2-104">語法</span><span class="sxs-lookup"><span data-stu-id="546e2-104">SYNTAX</span></span>

### <span data-ttu-id="546e2-105">SetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="546e2-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="546e2-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="546e2-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546e2-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="546e2-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546e2-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="546e2-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="546e2-109">描述</span><span class="sxs-lookup"><span data-stu-id="546e2-109">DESCRIPTION</span></span>
<span data-ttu-id="546e2-110">**Set-AzApiManagementPolidlet** 會設定 API 管理的指定範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="546e2-111">例子</span><span class="sxs-lookup"><span data-stu-id="546e2-111">EXAMPLES</span></span>

### <span data-ttu-id="546e2-112">範例 1：設定租使用者層級策略</span><span class="sxs-lookup"><span data-stu-id="546e2-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="546e2-113">此命令會從名為 tenantpolicy.xml 的檔案設定租使用者層級tenantpolicy.xml。</span><span class="sxs-lookup"><span data-stu-id="546e2-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="546e2-114">範例 2：設定產品範圍策略</span><span class="sxs-lookup"><span data-stu-id="546e2-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="546e2-115">此命令會設定 API 管理的產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="546e2-116">範例 3：設定 API 範圍策略</span><span class="sxs-lookup"><span data-stu-id="546e2-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="546e2-117">此命令會設定 API 管理的 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="546e2-118">範例 4：設定作業範圍策略</span><span class="sxs-lookup"><span data-stu-id="546e2-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="546e2-119">此命令會設定 API 管理的作業範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="546e2-120">參數</span><span class="sxs-lookup"><span data-stu-id="546e2-120">PARAMETERS</span></span>

### <span data-ttu-id="546e2-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="546e2-121">-ApiId</span></span>
<span data-ttu-id="546e2-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="546e2-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="546e2-123">如果您指定此參數，Cmdlet 會設定 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546e2-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="546e2-124">-ApiRevision</span></span>
<span data-ttu-id="546e2-125">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="546e2-125">Identifier of API Revision.</span></span> <span data-ttu-id="546e2-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="546e2-126">This parameter is optional.</span></span> <span data-ttu-id="546e2-127">如果未指定，將會更新目前使用中的 api 修訂中的該政策。</span><span class="sxs-lookup"><span data-stu-id="546e2-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546e2-128">-內容</span><span class="sxs-lookup"><span data-stu-id="546e2-128">-Context</span></span>
<span data-ttu-id="546e2-129">指定 **PsApiManagementCoNtext 的實例**。</span><span class="sxs-lookup"><span data-stu-id="546e2-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="546e2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546e2-130">-DefaultProfile</span></span>
<span data-ttu-id="546e2-131">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="546e2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="546e2-132">-格式</span><span class="sxs-lookup"><span data-stu-id="546e2-132">-Format</span></span>
<span data-ttu-id="546e2-133">指定策略的格式。</span><span class="sxs-lookup"><span data-stu-id="546e2-133">Specifies the format of the policy.</span></span> <span data-ttu-id="546e2-134">使用時 `application/vnd.ms-azure-apim.policy+xml` ，該策略中包含的運算式必須能逸出 XML。</span><span class="sxs-lookup"><span data-stu-id="546e2-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="546e2-135">使用 `application/vnd.ms-azure-apim.policy.raw+xml` 時 **，不需要** 使用 XML 逸出該策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="546e2-136">預設值為 `application/vnd.ms-azure-apim.policy+xml` 。</span><span class="sxs-lookup"><span data-stu-id="546e2-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="546e2-137">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="546e2-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="546e2-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="546e2-138">-OperationId</span></span>
<span data-ttu-id="546e2-139">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="546e2-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="546e2-140">如果使用 ApiId 指定，將會設定作業範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="546e2-141">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="546e2-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546e2-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="546e2-142">-PassThru</span></span>
<span data-ttu-id="546e2-143">Passthru</span><span class="sxs-lookup"><span data-stu-id="546e2-143">passthru</span></span>

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

### <span data-ttu-id="546e2-144">-策略</span><span class="sxs-lookup"><span data-stu-id="546e2-144">-Policy</span></span>
<span data-ttu-id="546e2-145">將政策檔指定為字串。</span><span class="sxs-lookup"><span data-stu-id="546e2-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="546e2-146">如果未指定 -*PolicyFilePath，* 則此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="546e2-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="546e2-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="546e2-147">-PolicyFilePath</span></span>
<span data-ttu-id="546e2-148">指定策略檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="546e2-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="546e2-149">如果未指定 Policy 參數，則此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="546e2-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="546e2-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="546e2-150">-PolicyUrl</span></span>
<span data-ttu-id="546e2-151">主託管策略檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="546e2-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="546e2-152">未指定 -Policy 或 -PolicyFilePath 時，需要此參數。</span><span class="sxs-lookup"><span data-stu-id="546e2-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="546e2-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="546e2-153">-ProductId</span></span>
<span data-ttu-id="546e2-154">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="546e2-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="546e2-155">如果指定此參數，Cmdlet 會設定產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="546e2-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546e2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546e2-156">CommonParameters</span></span>
<span data-ttu-id="546e2-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="546e2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546e2-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="546e2-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546e2-159">輸入</span><span class="sxs-lookup"><span data-stu-id="546e2-159">INPUTS</span></span>

### <span data-ttu-id="546e2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="546e2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="546e2-161">System.String</span><span class="sxs-lookup"><span data-stu-id="546e2-161">System.String</span></span>

### <span data-ttu-id="546e2-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="546e2-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="546e2-163">輸出</span><span class="sxs-lookup"><span data-stu-id="546e2-163">OUTPUTS</span></span>

### <span data-ttu-id="546e2-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="546e2-164">System.Boolean</span></span>

## <span data-ttu-id="546e2-165">筆記</span><span class="sxs-lookup"><span data-stu-id="546e2-165">NOTES</span></span>

## <span data-ttu-id="546e2-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="546e2-166">RELATED LINKS</span></span>

[<span data-ttu-id="546e2-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="546e2-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="546e2-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="546e2-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


