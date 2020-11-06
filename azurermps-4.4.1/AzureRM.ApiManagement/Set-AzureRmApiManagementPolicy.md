---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450089"
---
# <span data-ttu-id="49b47-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="49b47-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="49b47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49b47-102">SYNOPSIS</span></span>
<span data-ttu-id="49b47-103">設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b47-104">句法</span><span class="sxs-lookup"><span data-stu-id="49b47-104">SYNTAX</span></span>

### <span data-ttu-id="49b47-105">租使用者層級 (預設) </span><span class="sxs-lookup"><span data-stu-id="49b47-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49b47-106">產品層級</span><span class="sxs-lookup"><span data-stu-id="49b47-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49b47-107">API 層級</span><span class="sxs-lookup"><span data-stu-id="49b47-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49b47-108">操作層級</span><span class="sxs-lookup"><span data-stu-id="49b47-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b47-109">說明</span><span class="sxs-lookup"><span data-stu-id="49b47-109">DESCRIPTION</span></span>
<span data-ttu-id="49b47-110">**AzureRmApiManagementPolicy** Cmdlet 會設定 API 管理的指定範圍原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="49b47-111">示例</span><span class="sxs-lookup"><span data-stu-id="49b47-111">EXAMPLES</span></span>

### <span data-ttu-id="49b47-112">範例1：設定租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="49b47-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="49b47-113">這個命令會從名為 tenantpolicy.xml 的檔案設定租使用者層級原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="49b47-114">範例2：設定產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="49b47-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="49b47-115">這個命令會設定 API 管理的產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="49b47-116">範例3：設定 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="49b47-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="49b47-117">這個命令會針對 API 管理設定 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="49b47-118">範例4：設定操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="49b47-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="49b47-119">這個命令會設定 API 管理的操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="49b47-120">參數</span><span class="sxs-lookup"><span data-stu-id="49b47-120">PARAMETERS</span></span>

### <span data-ttu-id="49b47-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="49b47-121">-ApiId</span></span>
<span data-ttu-id="49b47-122">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49b47-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="49b47-123">如果您指定此參數，則 Cmdlet 會設定 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="49b47-124">-內容</span><span class="sxs-lookup"><span data-stu-id="49b47-124">-Context</span></span>
<span data-ttu-id="49b47-125">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="49b47-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="49b47-126">-Format</span><span class="sxs-lookup"><span data-stu-id="49b47-126">-Format</span></span>
<span data-ttu-id="49b47-127">指定原則的格式。</span><span class="sxs-lookup"><span data-stu-id="49b47-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="49b47-128">預設值為 "application/vnd. ms-azure-apim. policy + xml"。</span><span class="sxs-lookup"><span data-stu-id="49b47-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="49b47-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="49b47-129">-OperationId</span></span>
<span data-ttu-id="49b47-130">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49b47-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="49b47-131">如果以 ApiId 指定，將會設定 operation 作用中原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="49b47-132">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="49b47-132">This parameters is required.</span></span>

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

### <span data-ttu-id="49b47-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49b47-133">-PassThru</span></span>
<span data-ttu-id="49b47-134">passthru</span><span class="sxs-lookup"><span data-stu-id="49b47-134">passthru</span></span>

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

### <span data-ttu-id="49b47-135">-原則</span><span class="sxs-lookup"><span data-stu-id="49b47-135">-Policy</span></span>
<span data-ttu-id="49b47-136">指定原則檔做為字串。</span><span class="sxs-lookup"><span data-stu-id="49b47-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="49b47-137">如果未指定- *PolicyFilePath* ，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="49b47-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="49b47-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="49b47-138">-PolicyFilePath</span></span>
<span data-ttu-id="49b47-139">指定原則檔路徑。</span><span class="sxs-lookup"><span data-stu-id="49b47-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="49b47-140">如果未指定 *原則* 參數，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="49b47-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="49b47-141">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="49b47-141">-ProductId</span></span>
<span data-ttu-id="49b47-142">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49b47-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="49b47-143">如果指定此參數，則 Cmdlet 會設定產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="49b47-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="49b47-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b47-144">-DefaultProfile</span></span>
<span data-ttu-id="49b47-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49b47-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b47-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b47-146">CommonParameters</span></span>
<span data-ttu-id="49b47-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49b47-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b47-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49b47-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b47-149">輸入</span><span class="sxs-lookup"><span data-stu-id="49b47-149">INPUTS</span></span>

## <span data-ttu-id="49b47-150">輸出</span><span class="sxs-lookup"><span data-stu-id="49b47-150">OUTPUTS</span></span>

### <span data-ttu-id="49b47-151">bool</span><span class="sxs-lookup"><span data-stu-id="49b47-151">bool</span></span>

## <span data-ttu-id="49b47-152">筆記</span><span class="sxs-lookup"><span data-stu-id="49b47-152">NOTES</span></span>

## <span data-ttu-id="49b47-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="49b47-153">RELATED LINKS</span></span>

[<span data-ttu-id="49b47-154">AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="49b47-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="49b47-155">移除-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="49b47-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


