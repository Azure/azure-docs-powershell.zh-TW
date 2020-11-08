---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138375"
---
# <span data-ttu-id="23017-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="23017-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="23017-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23017-102">SYNOPSIS</span></span>
<span data-ttu-id="23017-103">建立新的命名值。</span><span class="sxs-lookup"><span data-stu-id="23017-103">Creates new Named Value.</span></span>

## <span data-ttu-id="23017-104">句法</span><span class="sxs-lookup"><span data-stu-id="23017-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23017-105">說明</span><span class="sxs-lookup"><span data-stu-id="23017-105">DESCRIPTION</span></span>
<span data-ttu-id="23017-106">**新的-AzApiManagementNamedValue** Cmdlet 會建立 **名為** 「Azure API 管理」的值。</span><span class="sxs-lookup"><span data-stu-id="23017-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="23017-107">示例</span><span class="sxs-lookup"><span data-stu-id="23017-107">EXAMPLES</span></span>

### <span data-ttu-id="23017-108">範例1：建立包含標記的命名值</span><span class="sxs-lookup"><span data-stu-id="23017-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="23017-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="23017-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="23017-110">第二個命令會建立一個命名值，並將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="23017-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="23017-111">範例2：建立具有機密值的命名值</span><span class="sxs-lookup"><span data-stu-id="23017-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="23017-112">這個命令會建立一個含有已加密之值的 **命名值** 。</span><span class="sxs-lookup"><span data-stu-id="23017-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="23017-113">參數</span><span class="sxs-lookup"><span data-stu-id="23017-113">PARAMETERS</span></span>

### <span data-ttu-id="23017-114">-內容</span><span class="sxs-lookup"><span data-stu-id="23017-114">-Context</span></span>
<span data-ttu-id="23017-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="23017-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="23017-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="23017-116">This parameter is required.</span></span>

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

### <span data-ttu-id="23017-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23017-117">-DefaultProfile</span></span>
<span data-ttu-id="23017-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23017-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23017-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="23017-119">-Name</span></span>
<span data-ttu-id="23017-120">命名值的名稱。</span><span class="sxs-lookup"><span data-stu-id="23017-120">Name of the named value.</span></span>
<span data-ttu-id="23017-121">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="23017-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="23017-122">它可能只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="23017-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="23017-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="23017-123">This parameter is required.</span></span>

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

### <span data-ttu-id="23017-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="23017-124">-NamedValueId</span></span>
<span data-ttu-id="23017-125">新命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="23017-125">Identifier of new named value.</span></span>
<span data-ttu-id="23017-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="23017-126">This parameter is optional.</span></span>
<span data-ttu-id="23017-127">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="23017-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="23017-128">密碼</span><span class="sxs-lookup"><span data-stu-id="23017-128">-Secret</span></span>
<span data-ttu-id="23017-129">判斷值是否為秘密，且應該加密。</span><span class="sxs-lookup"><span data-stu-id="23017-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="23017-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="23017-130">This parameter is optional.</span></span>
<span data-ttu-id="23017-131">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="23017-131">Default Value is false.</span></span>

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

### <span data-ttu-id="23017-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="23017-132">-Tag</span></span>
<span data-ttu-id="23017-133">要與命名值相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="23017-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="23017-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="23017-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="23017-135">-值</span><span class="sxs-lookup"><span data-stu-id="23017-135">-Value</span></span>
<span data-ttu-id="23017-136">命名值的值。</span><span class="sxs-lookup"><span data-stu-id="23017-136">Value of the named value.</span></span>
<span data-ttu-id="23017-137">可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="23017-137">Can contain policy expressions.</span></span>
<span data-ttu-id="23017-138">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="23017-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="23017-139">它不可以是空白或只由空白組成。</span><span class="sxs-lookup"><span data-stu-id="23017-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="23017-140">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="23017-140">This parameter is required.</span></span>

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

### <span data-ttu-id="23017-141">-確認</span><span class="sxs-lookup"><span data-stu-id="23017-141">-Confirm</span></span>
<span data-ttu-id="23017-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23017-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23017-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23017-143">-WhatIf</span></span>
<span data-ttu-id="23017-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23017-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23017-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23017-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23017-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23017-146">CommonParameters</span></span>
<span data-ttu-id="23017-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23017-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23017-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23017-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23017-149">輸入</span><span class="sxs-lookup"><span data-stu-id="23017-149">INPUTS</span></span>

### <span data-ttu-id="23017-150">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="23017-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23017-151">System.object</span><span class="sxs-lookup"><span data-stu-id="23017-151">System.String</span></span>

### <span data-ttu-id="23017-152">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="23017-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="23017-153">System.object []</span><span class="sxs-lookup"><span data-stu-id="23017-153">System.String[]</span></span>

## <span data-ttu-id="23017-154">輸出</span><span class="sxs-lookup"><span data-stu-id="23017-154">OUTPUTS</span></span>

### <span data-ttu-id="23017-155">ServiceManagement. PsApiManagementNamedValue （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="23017-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="23017-156">筆記</span><span class="sxs-lookup"><span data-stu-id="23017-156">NOTES</span></span>

## <span data-ttu-id="23017-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="23017-157">RELATED LINKS</span></span>
