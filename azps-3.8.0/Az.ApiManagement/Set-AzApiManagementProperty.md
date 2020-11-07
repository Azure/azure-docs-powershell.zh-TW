---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 38c937de07d4a19a6c2632356c2b9ac58b2b416a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965616"
---
# <span data-ttu-id="978d1-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="978d1-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="978d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="978d1-102">SYNOPSIS</span></span>
<span data-ttu-id="978d1-103">修改 API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="978d1-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="978d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="978d1-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="978d1-105">DESCRIPTION</span></span>
<span data-ttu-id="978d1-106">**AzApiManagementProperty** Cmdlet 會修改 Azure API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="978d1-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="978d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="978d1-107">EXAMPLES</span></span>

### <span data-ttu-id="978d1-108">範例1：變更屬性上的標記</span><span class="sxs-lookup"><span data-stu-id="978d1-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="978d1-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="978d1-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="978d1-110">第二個命令會修改 ID 為 Property11 的屬性。</span><span class="sxs-lookup"><span data-stu-id="978d1-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="978d1-111">命令會將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="978d1-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="978d1-112">範例2：修改屬性以有機密值</span><span class="sxs-lookup"><span data-stu-id="978d1-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="978d1-113">這個命令會將屬性變更為已加密。</span><span class="sxs-lookup"><span data-stu-id="978d1-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="978d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="978d1-114">PARAMETERS</span></span>

### <span data-ttu-id="978d1-115">-內容</span><span class="sxs-lookup"><span data-stu-id="978d1-115">-Context</span></span>
<span data-ttu-id="978d1-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="978d1-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="978d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978d1-117">-DefaultProfile</span></span>
<span data-ttu-id="978d1-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="978d1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="978d1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="978d1-119">-Name</span></span>
<span data-ttu-id="978d1-120">指定屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="978d1-120">Specifies the name of the property.</span></span>
<span data-ttu-id="978d1-121">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="978d1-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="978d1-122">名稱只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="978d1-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="978d1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="978d1-123">-PassThru</span></span>
<span data-ttu-id="978d1-124">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementProperty** 。</span><span class="sxs-lookup"><span data-stu-id="978d1-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="978d1-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="978d1-125">-PropertyId</span></span>
<span data-ttu-id="978d1-126">指定此 Cmdlet 所修改之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="978d1-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="978d1-127">密碼</span><span class="sxs-lookup"><span data-stu-id="978d1-127">-Secret</span></span>
<span data-ttu-id="978d1-128">表示屬性值是一個機密，應該經過加密。</span><span class="sxs-lookup"><span data-stu-id="978d1-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978d1-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="978d1-129">-Tag</span></span>
<span data-ttu-id="978d1-130">與屬性相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="978d1-130">Tags associated with a property.</span></span> <span data-ttu-id="978d1-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="978d1-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="978d1-132">-值</span><span class="sxs-lookup"><span data-stu-id="978d1-132">-Value</span></span>
<span data-ttu-id="978d1-133">指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="978d1-133">Specifies a value for the property.</span></span>
<span data-ttu-id="978d1-134">這個值可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="978d1-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="978d1-135">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="978d1-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="978d1-136">此值可能不是空白，或是只由空格所組成。</span><span class="sxs-lookup"><span data-stu-id="978d1-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="978d1-137">-確認</span><span class="sxs-lookup"><span data-stu-id="978d1-137">-Confirm</span></span>
<span data-ttu-id="978d1-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="978d1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978d1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978d1-139">-WhatIf</span></span>
<span data-ttu-id="978d1-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="978d1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="978d1-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="978d1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978d1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978d1-142">CommonParameters</span></span>
<span data-ttu-id="978d1-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="978d1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978d1-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="978d1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978d1-145">輸入</span><span class="sxs-lookup"><span data-stu-id="978d1-145">INPUTS</span></span>

### <span data-ttu-id="978d1-146">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="978d1-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="978d1-147">System.object</span><span class="sxs-lookup"><span data-stu-id="978d1-147">System.String</span></span>

### <span data-ttu-id="978d1-148">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="978d1-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="978d1-149">System.object []</span><span class="sxs-lookup"><span data-stu-id="978d1-149">System.String[]</span></span>

### <span data-ttu-id="978d1-150">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="978d1-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="978d1-151">輸出</span><span class="sxs-lookup"><span data-stu-id="978d1-151">OUTPUTS</span></span>

### <span data-ttu-id="978d1-152">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="978d1-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="978d1-153">筆記</span><span class="sxs-lookup"><span data-stu-id="978d1-153">NOTES</span></span>

## <span data-ttu-id="978d1-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="978d1-154">RELATED LINKS</span></span>

[<span data-ttu-id="978d1-155">AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="978d1-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="978d1-156">新-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="978d1-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="978d1-157">移除-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="978d1-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


