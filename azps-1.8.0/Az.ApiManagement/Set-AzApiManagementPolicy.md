---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 495e076a58d4cb1f19de4f9b7eb740e14aa7b407
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788749"
---
# <span data-ttu-id="d1df3-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1df3-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="d1df3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1df3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1df3-103">設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="d1df3-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1df3-104">SYNTAX</span></span>

### <span data-ttu-id="d1df3-105">SetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="d1df3-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1df3-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="d1df3-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1df3-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="d1df3-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1df3-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="d1df3-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1df3-109">說明</span><span class="sxs-lookup"><span data-stu-id="d1df3-109">DESCRIPTION</span></span>
<span data-ttu-id="d1df3-110">**AzApiManagementPolicy** Cmdlet 會設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="d1df3-111">示例</span><span class="sxs-lookup"><span data-stu-id="d1df3-111">EXAMPLES</span></span>

### <span data-ttu-id="d1df3-112">範例1：設定租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="d1df3-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="d1df3-113">這個命令會從名為 tenantpolicy.xml 的檔案設定租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="d1df3-114">範例2：設定產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="d1df3-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="d1df3-115">這個命令會設定 API 管理的產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="d1df3-116">範例3：設定 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="d1df3-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="d1df3-117">這個命令會針對 API 管理設定 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="d1df3-118">範例4：設定操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="d1df3-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="d1df3-119">這個命令會設定 API 管理的操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="d1df3-120">參數</span><span class="sxs-lookup"><span data-stu-id="d1df3-120">PARAMETERS</span></span>

### <span data-ttu-id="d1df3-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1df3-121">-ApiId</span></span>
<span data-ttu-id="d1df3-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1df3-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="d1df3-123">如果您指定此參數，則 Cmdlet 會設定 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="d1df3-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d1df3-124">-ApiRevision</span></span>
<span data-ttu-id="d1df3-125">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1df3-125">Identifier of API Revision.</span></span> <span data-ttu-id="d1df3-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d1df3-126">This parameter is optional.</span></span> <span data-ttu-id="d1df3-127">如果未指定，原則將會在目前使用中的 api 修正程式中更新。</span><span class="sxs-lookup"><span data-stu-id="d1df3-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="d1df3-128">-內容</span><span class="sxs-lookup"><span data-stu-id="d1df3-128">-Context</span></span>
<span data-ttu-id="d1df3-129">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="d1df3-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="d1df3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1df3-130">-DefaultProfile</span></span>
<span data-ttu-id="d1df3-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1df3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1df3-132">-Format</span><span class="sxs-lookup"><span data-stu-id="d1df3-132">-Format</span></span>
<span data-ttu-id="d1df3-133">指定原則的格式。</span><span class="sxs-lookup"><span data-stu-id="d1df3-133">Specifies the format of the policy.</span></span> <span data-ttu-id="d1df3-134">當使用時 `application/vnd.ms-az-apim.policy+xml` ，在原則中包含的運算式必須是以 XML 轉義的。</span><span class="sxs-lookup"><span data-stu-id="d1df3-134">When using `application/vnd.ms-az-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="d1df3-135">`application/vnd.ms-az-apim.policy.raw+xml`若要將原則用於 XML 轉義，則 **不** 需要使用它。</span><span class="sxs-lookup"><span data-stu-id="d1df3-135">When using `application/vnd.ms-az-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="d1df3-136">預設值為 `application/vnd.ms-az-apim.policy+xml` 。</span><span class="sxs-lookup"><span data-stu-id="d1df3-136">The default value is `application/vnd.ms-az-apim.policy+xml`.</span></span>
<span data-ttu-id="d1df3-137">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d1df3-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1df3-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d1df3-138">-OperationId</span></span>
<span data-ttu-id="d1df3-139">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1df3-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="d1df3-140">如果以 ApiId 指定，將會設定 operation 作用中原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="d1df3-141">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="d1df3-141">This parameters is required.</span></span>

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

### <span data-ttu-id="d1df3-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1df3-142">-PassThru</span></span>
<span data-ttu-id="d1df3-143">passthru</span><span class="sxs-lookup"><span data-stu-id="d1df3-143">passthru</span></span>

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

### <span data-ttu-id="d1df3-144">-原則</span><span class="sxs-lookup"><span data-stu-id="d1df3-144">-Policy</span></span>
<span data-ttu-id="d1df3-145">指定原則檔做為字串。</span><span class="sxs-lookup"><span data-stu-id="d1df3-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="d1df3-146">如果未指定- *PolicyFilePath* ，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="d1df3-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="d1df3-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="d1df3-147">-PolicyFilePath</span></span>
<span data-ttu-id="d1df3-148">指定原則檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d1df3-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="d1df3-149">如果未指定 *原則* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="d1df3-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="d1df3-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="d1df3-150">-PolicyUrl</span></span>
<span data-ttu-id="d1df3-151">託管原則檔的 Url。</span><span class="sxs-lookup"><span data-stu-id="d1df3-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="d1df3-152">如果未指定-Policy 或-PolicyFilePath，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="d1df3-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="d1df3-153">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="d1df3-153">-ProductId</span></span>
<span data-ttu-id="d1df3-154">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1df3-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="d1df3-155">如果指定此參數，則 Cmdlet 會設定產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="d1df3-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="d1df3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1df3-156">CommonParameters</span></span>
<span data-ttu-id="d1df3-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1df3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1df3-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1df3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1df3-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d1df3-159">INPUTS</span></span>

### <span data-ttu-id="d1df3-160">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d1df3-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1df3-161">System.object</span><span class="sxs-lookup"><span data-stu-id="d1df3-161">System.String</span></span>

### <span data-ttu-id="d1df3-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d1df3-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1df3-163">輸出</span><span class="sxs-lookup"><span data-stu-id="d1df3-163">OUTPUTS</span></span>

### <span data-ttu-id="d1df3-164">System.object</span><span class="sxs-lookup"><span data-stu-id="d1df3-164">System.Boolean</span></span>

## <span data-ttu-id="d1df3-165">筆記</span><span class="sxs-lookup"><span data-stu-id="d1df3-165">NOTES</span></span>

## <span data-ttu-id="d1df3-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1df3-166">RELATED LINKS</span></span>

[<span data-ttu-id="d1df3-167">AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1df3-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="d1df3-168">移除-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1df3-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


