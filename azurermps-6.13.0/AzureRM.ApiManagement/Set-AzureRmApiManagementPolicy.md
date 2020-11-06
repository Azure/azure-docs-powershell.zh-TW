---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445808"
---
# <span data-ttu-id="ee8d8-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee8d8-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="ee8d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8d8-103">設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee8d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee8d8-104">SYNTAX</span></span>

### <span data-ttu-id="ee8d8-105">SetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="ee8d8-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee8d8-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="ee8d8-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee8d8-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="ee8d8-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee8d8-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="ee8d8-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee8d8-109">說明</span><span class="sxs-lookup"><span data-stu-id="ee8d8-109">DESCRIPTION</span></span>
<span data-ttu-id="ee8d8-110">**AzureRmApiManagementPolicy** Cmdlet 會設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="ee8d8-111">示例</span><span class="sxs-lookup"><span data-stu-id="ee8d8-111">EXAMPLES</span></span>

### <span data-ttu-id="ee8d8-112">範例1：設定租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="ee8d8-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="ee8d8-113">這個命令會從名為 tenantpolicy.xml 的檔案設定租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="ee8d8-114">範例2：設定產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="ee8d8-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="ee8d8-115">這個命令會設定 API 管理的產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="ee8d8-116">範例3：設定 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="ee8d8-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="ee8d8-117">這個命令會針對 API 管理設定 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="ee8d8-118">範例4：設定操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="ee8d8-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="ee8d8-119">這個命令會設定 API 管理的操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="ee8d8-120">參數</span><span class="sxs-lookup"><span data-stu-id="ee8d8-120">PARAMETERS</span></span>

### <span data-ttu-id="ee8d8-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ee8d8-121">-ApiId</span></span>
<span data-ttu-id="ee8d8-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="ee8d8-123">如果您指定此參數，則 Cmdlet 會設定 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="ee8d8-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ee8d8-124">-ApiRevision</span></span>
<span data-ttu-id="ee8d8-125">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-125">Identifier of API Revision.</span></span> <span data-ttu-id="ee8d8-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-126">This parameter is optional.</span></span> <span data-ttu-id="ee8d8-127">如果未指定，原則將會在目前使用中的 api 修正程式中更新。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="ee8d8-128">-內容</span><span class="sxs-lookup"><span data-stu-id="ee8d8-128">-Context</span></span>
<span data-ttu-id="ee8d8-129">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ee8d8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8d8-130">-DefaultProfile</span></span>
<span data-ttu-id="ee8d8-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee8d8-132">-Format</span><span class="sxs-lookup"><span data-stu-id="ee8d8-132">-Format</span></span>
<span data-ttu-id="ee8d8-133">指定原則的格式。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-133">Specifies the format of the policy.</span></span> <span data-ttu-id="ee8d8-134">當使用時 `application/vnd.ms-azure-apim.policy+xml` ，在原則中包含的運算式必須是以 XML 轉義的。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="ee8d8-135">`application/vnd.ms-azure-apim.policy.raw+xml`若要將原則用於 XML 轉義，則 **不** 需要使用它。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="ee8d8-136">預設值為 `application/vnd.ms-azure-apim.policy+xml` 。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="ee8d8-137">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="ee8d8-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ee8d8-138">-OperationId</span></span>
<span data-ttu-id="ee8d8-139">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="ee8d8-140">如果以 ApiId 指定，將會設定 operation 作用中原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="ee8d8-141">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-141">This parameters is required.</span></span>

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

### <span data-ttu-id="ee8d8-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee8d8-142">-PassThru</span></span>
<span data-ttu-id="ee8d8-143">passthru</span><span class="sxs-lookup"><span data-stu-id="ee8d8-143">passthru</span></span>

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

### <span data-ttu-id="ee8d8-144">-原則</span><span class="sxs-lookup"><span data-stu-id="ee8d8-144">-Policy</span></span>
<span data-ttu-id="ee8d8-145">指定原則檔做為字串。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="ee8d8-146">如果未指定- *PolicyFilePath* ，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="ee8d8-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="ee8d8-147">-PolicyFilePath</span></span>
<span data-ttu-id="ee8d8-148">指定原則檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="ee8d8-149">如果未指定 *原則* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="ee8d8-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="ee8d8-150">-PolicyUrl</span></span>
<span data-ttu-id="ee8d8-151">託管原則檔的 Url。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="ee8d8-152">如果未指定-Policy 或-PolicyFilePath，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="ee8d8-153">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="ee8d8-153">-ProductId</span></span>
<span data-ttu-id="ee8d8-154">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="ee8d8-155">如果指定此參數，則 Cmdlet 會設定產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="ee8d8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8d8-156">CommonParameters</span></span>
<span data-ttu-id="ee8d8-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8d8-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee8d8-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8d8-159">輸入</span><span class="sxs-lookup"><span data-stu-id="ee8d8-159">INPUTS</span></span>

### <span data-ttu-id="ee8d8-160">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ee8d8-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ee8d8-161">System.object</span><span class="sxs-lookup"><span data-stu-id="ee8d8-161">System.String</span></span>

### <span data-ttu-id="ee8d8-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ee8d8-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ee8d8-163">輸出</span><span class="sxs-lookup"><span data-stu-id="ee8d8-163">OUTPUTS</span></span>

### <span data-ttu-id="ee8d8-164">System.object</span><span class="sxs-lookup"><span data-stu-id="ee8d8-164">System.Boolean</span></span>

## <span data-ttu-id="ee8d8-165">筆記</span><span class="sxs-lookup"><span data-stu-id="ee8d8-165">NOTES</span></span>

## <span data-ttu-id="ee8d8-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee8d8-166">RELATED LINKS</span></span>

[<span data-ttu-id="ee8d8-167">AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee8d8-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="ee8d8-168">移除-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ee8d8-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


