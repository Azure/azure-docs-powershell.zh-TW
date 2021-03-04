---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 43a8d9969668abd96783fd766d4f99edb4b89e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912938"
---
# <span data-ttu-id="282ed-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="282ed-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="282ed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="282ed-102">SYNOPSIS</span></span>
<span data-ttu-id="282ed-103">建立新的命名值。</span><span class="sxs-lookup"><span data-stu-id="282ed-103">Creates new Named Value.</span></span>

## <span data-ttu-id="282ed-104">語法</span><span class="sxs-lookup"><span data-stu-id="282ed-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="282ed-105">描述</span><span class="sxs-lookup"><span data-stu-id="282ed-105">DESCRIPTION</span></span>
<span data-ttu-id="282ed-106">**New-AzApiManagementNamedValue** Cmdlet 會建立 Azure API 管理 **具名值**。</span><span class="sxs-lookup"><span data-stu-id="282ed-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="282ed-107">例子</span><span class="sxs-lookup"><span data-stu-id="282ed-107">EXAMPLES</span></span>

### <span data-ttu-id="282ed-108">範例 1：建立包含標記的命名值</span><span class="sxs-lookup"><span data-stu-id="282ed-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="282ed-109">第一個命令會指派兩個值給$Tags變數。</span><span class="sxs-lookup"><span data-stu-id="282ed-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="282ed-110">第二個命令會建立一個命名值，並將$Tags做為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="282ed-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="282ed-111">範例 2：建立具有機密值的命名值</span><span class="sxs-lookup"><span data-stu-id="282ed-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="282ed-112">此命令會 **建立具有加密** 值的命名值。</span><span class="sxs-lookup"><span data-stu-id="282ed-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="282ed-113">參數</span><span class="sxs-lookup"><span data-stu-id="282ed-113">PARAMETERS</span></span>

### <span data-ttu-id="282ed-114">-內容</span><span class="sxs-lookup"><span data-stu-id="282ed-114">-Context</span></span>
<span data-ttu-id="282ed-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="282ed-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="282ed-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="282ed-116">This parameter is required.</span></span>

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

### <span data-ttu-id="282ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282ed-117">-DefaultProfile</span></span>
<span data-ttu-id="282ed-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="282ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="282ed-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="282ed-119">-Name</span></span>
<span data-ttu-id="282ed-120">已命名值的名稱。</span><span class="sxs-lookup"><span data-stu-id="282ed-120">Name of the named value.</span></span>
<span data-ttu-id="282ed-121">長度上限為 100 個字元。</span><span class="sxs-lookup"><span data-stu-id="282ed-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="282ed-122">它可能只包含字母、數位、期間、虛線和虛線字元。</span><span class="sxs-lookup"><span data-stu-id="282ed-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="282ed-123">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="282ed-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282ed-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="282ed-124">-NamedValueId</span></span>
<span data-ttu-id="282ed-125">新命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="282ed-125">Identifier of new named value.</span></span>
<span data-ttu-id="282ed-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="282ed-126">This parameter is optional.</span></span>
<span data-ttu-id="282ed-127">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="282ed-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="282ed-128">-機密</span><span class="sxs-lookup"><span data-stu-id="282ed-128">-Secret</span></span>
<span data-ttu-id="282ed-129">判斷值是否為機密，是否應該加密。</span><span class="sxs-lookup"><span data-stu-id="282ed-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="282ed-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="282ed-130">This parameter is optional.</span></span>
<span data-ttu-id="282ed-131">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="282ed-131">Default Value is false.</span></span>

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

### <span data-ttu-id="282ed-132">-標記</span><span class="sxs-lookup"><span data-stu-id="282ed-132">-Tag</span></span>
<span data-ttu-id="282ed-133">與指定值相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="282ed-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="282ed-134">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="282ed-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282ed-135">-值</span><span class="sxs-lookup"><span data-stu-id="282ed-135">-Value</span></span>
<span data-ttu-id="282ed-136">已命名值的值。</span><span class="sxs-lookup"><span data-stu-id="282ed-136">Value of the named value.</span></span>
<span data-ttu-id="282ed-137">可以包含策略運算式。</span><span class="sxs-lookup"><span data-stu-id="282ed-137">Can contain policy expressions.</span></span>
<span data-ttu-id="282ed-138">長度上限為 1000 個字元。</span><span class="sxs-lookup"><span data-stu-id="282ed-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="282ed-139">它不能是空白的，或僅包含空格。</span><span class="sxs-lookup"><span data-stu-id="282ed-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="282ed-140">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="282ed-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282ed-141">-確認</span><span class="sxs-lookup"><span data-stu-id="282ed-141">-Confirm</span></span>
<span data-ttu-id="282ed-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="282ed-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="282ed-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="282ed-143">-WhatIf</span></span>
<span data-ttu-id="282ed-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="282ed-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="282ed-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="282ed-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="282ed-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282ed-146">CommonParameters</span></span>
<span data-ttu-id="282ed-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="282ed-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282ed-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="282ed-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282ed-149">輸入</span><span class="sxs-lookup"><span data-stu-id="282ed-149">INPUTS</span></span>

### <span data-ttu-id="282ed-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="282ed-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="282ed-151">System.String</span><span class="sxs-lookup"><span data-stu-id="282ed-151">System.String</span></span>

### <span data-ttu-id="282ed-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="282ed-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="282ed-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="282ed-153">System.String[]</span></span>

## <span data-ttu-id="282ed-154">輸出</span><span class="sxs-lookup"><span data-stu-id="282ed-154">OUTPUTS</span></span>

### <span data-ttu-id="282ed-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="282ed-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="282ed-156">筆記</span><span class="sxs-lookup"><span data-stu-id="282ed-156">NOTES</span></span>

## <span data-ttu-id="282ed-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="282ed-157">RELATED LINKS</span></span>
