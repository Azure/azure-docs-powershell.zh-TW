---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624106"
---
# <span data-ttu-id="1c9fa-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9fa-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="1c9fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9fa-103">設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c9fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c9fa-104">SYNTAX</span></span>

### <span data-ttu-id="1c9fa-105">SetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="1c9fa-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9fa-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="1c9fa-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c9fa-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="1c9fa-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c9fa-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="1c9fa-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c9fa-109">說明</span><span class="sxs-lookup"><span data-stu-id="1c9fa-109">DESCRIPTION</span></span>
<span data-ttu-id="1c9fa-110">**AzureRmApiManagementPolicy** Cmdlet 會設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="1c9fa-111">示例</span><span class="sxs-lookup"><span data-stu-id="1c9fa-111">EXAMPLES</span></span>

### <span data-ttu-id="1c9fa-112">範例1：設定租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="1c9fa-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="1c9fa-113">這個命令會從名為 tenantpolicy.xml 的檔案設定租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="1c9fa-114">範例2：設定產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="1c9fa-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="1c9fa-115">這個命令會設定 API 管理的產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="1c9fa-116">範例3：設定 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="1c9fa-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="1c9fa-117">這個命令會針對 API 管理設定 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="1c9fa-118">範例4：設定操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="1c9fa-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="1c9fa-119">這個命令會設定 API 管理的操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="1c9fa-120">參數</span><span class="sxs-lookup"><span data-stu-id="1c9fa-120">PARAMETERS</span></span>

### <span data-ttu-id="1c9fa-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1c9fa-121">-ApiId</span></span>
<span data-ttu-id="1c9fa-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="1c9fa-123">如果您指定此參數，則 Cmdlet 會設定 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9fa-124">-內容</span><span class="sxs-lookup"><span data-stu-id="1c9fa-124">-Context</span></span>
<span data-ttu-id="1c9fa-125">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1c9fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9fa-126">-DefaultProfile</span></span>
<span data-ttu-id="1c9fa-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1c9fa-128">-Format</span><span class="sxs-lookup"><span data-stu-id="1c9fa-128">-Format</span></span>
<span data-ttu-id="1c9fa-129">指定原則的格式。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="1c9fa-130">預設值為 "application/vnd. ms-azure-apim. policy + xml"。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="1c9fa-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1c9fa-131">-OperationId</span></span>
<span data-ttu-id="1c9fa-132">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="1c9fa-133">如果以 ApiId 指定，將會設定 operation 作用中原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="1c9fa-134">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9fa-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c9fa-135">-PassThru</span></span>
<span data-ttu-id="1c9fa-136">passthru</span><span class="sxs-lookup"><span data-stu-id="1c9fa-136">passthru</span></span>

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

### <span data-ttu-id="1c9fa-137">-原則</span><span class="sxs-lookup"><span data-stu-id="1c9fa-137">-Policy</span></span>
<span data-ttu-id="1c9fa-138">指定原則檔做為字串。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="1c9fa-139">如果未指定- *PolicyFilePath* ，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="1c9fa-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="1c9fa-140">-PolicyFilePath</span></span>
<span data-ttu-id="1c9fa-141">指定原則檔路徑。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="1c9fa-142">如果未指定 *原則* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="1c9fa-143">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="1c9fa-143">-ProductId</span></span>
<span data-ttu-id="1c9fa-144">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="1c9fa-145">如果指定此參數，則 Cmdlet 會設定產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9fa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9fa-146">CommonParameters</span></span>
<span data-ttu-id="1c9fa-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9fa-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9fa-149">輸入</span><span class="sxs-lookup"><span data-stu-id="1c9fa-149">INPUTS</span></span>

### <span data-ttu-id="1c9fa-150">所有</span><span class="sxs-lookup"><span data-stu-id="1c9fa-150">None</span></span>
<span data-ttu-id="1c9fa-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c9fa-152">輸出</span><span class="sxs-lookup"><span data-stu-id="1c9fa-152">OUTPUTS</span></span>

### <span data-ttu-id="1c9fa-153">bool</span><span class="sxs-lookup"><span data-stu-id="1c9fa-153">bool</span></span>

## <span data-ttu-id="1c9fa-154">筆記</span><span class="sxs-lookup"><span data-stu-id="1c9fa-154">NOTES</span></span>

## <span data-ttu-id="1c9fa-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c9fa-155">RELATED LINKS</span></span>

[<span data-ttu-id="1c9fa-156">AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9fa-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="1c9fa-157">移除-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9fa-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


