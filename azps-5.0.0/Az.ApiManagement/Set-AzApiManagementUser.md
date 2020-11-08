---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: d438294841becb1b65ba8b98452d13d067f2159d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139303"
---
# <span data-ttu-id="aa706-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aa706-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="aa706-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa706-102">SYNOPSIS</span></span>
<span data-ttu-id="aa706-103">設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aa706-103">Sets user details.</span></span>

## <span data-ttu-id="aa706-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa706-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa706-105">說明</span><span class="sxs-lookup"><span data-stu-id="aa706-105">DESCRIPTION</span></span>
<span data-ttu-id="aa706-106">**AzApiManagementUser** Cmdlet 會設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aa706-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="aa706-107">示例</span><span class="sxs-lookup"><span data-stu-id="aa706-107">EXAMPLES</span></span>

### <span data-ttu-id="aa706-108">範例1：變更使用者的密碼、電子郵件地址及狀態</span><span class="sxs-lookup"><span data-stu-id="aa706-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="aa706-109">這個命令會設定新的使用者密碼和電子郵件地址，並封鎖使用者。</span><span class="sxs-lookup"><span data-stu-id="aa706-109">This command sets a new user password and email address and blocks the user.</span></span>

### <span data-ttu-id="aa706-110">範例2</span><span class="sxs-lookup"><span data-stu-id="aa706-110">Example 2</span></span>

<span data-ttu-id="aa706-111">設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aa706-111">Sets user details.</span></span> <span data-ttu-id="aa706-112"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="aa706-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementUser -Context <PsApiManagementContext> -Email 'patti.fuller@contoso.com' -FirstName 'Patti' -LastName 'Fuller' -Password <SecureString> -State Active -UserId '0123456789'
```

## <span data-ttu-id="aa706-113">參數</span><span class="sxs-lookup"><span data-stu-id="aa706-113">PARAMETERS</span></span>

### <span data-ttu-id="aa706-114">-內容</span><span class="sxs-lookup"><span data-stu-id="aa706-114">-Context</span></span>
<span data-ttu-id="aa706-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="aa706-115">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="aa706-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="aa706-116">This parameter is required.</span></span>

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

### <span data-ttu-id="aa706-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa706-117">-DefaultProfile</span></span>
<span data-ttu-id="aa706-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa706-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa706-119">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="aa706-119">-Email</span></span>
<span data-ttu-id="aa706-120">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="aa706-120">Specifies the email address of the user.</span></span>
<span data-ttu-id="aa706-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="aa706-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa706-122">-FirstName</span><span class="sxs-lookup"><span data-stu-id="aa706-122">-FirstName</span></span>
<span data-ttu-id="aa706-123">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="aa706-123">Specifies the first name of the user.</span></span>
<span data-ttu-id="aa706-124">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="aa706-124">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="aa706-125">-LastName</span><span class="sxs-lookup"><span data-stu-id="aa706-125">-LastName</span></span>
<span data-ttu-id="aa706-126">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="aa706-126">Specifies the last name of the user.</span></span>
<span data-ttu-id="aa706-127">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="aa706-127">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="aa706-128">-記事</span><span class="sxs-lookup"><span data-stu-id="aa706-128">-Note</span></span>
<span data-ttu-id="aa706-129">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="aa706-129">Specifies a note about the user.</span></span>
<span data-ttu-id="aa706-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="aa706-130">This parameter is optional.</span></span>
<span data-ttu-id="aa706-131">此參數的預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="aa706-131">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="aa706-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa706-132">-PassThru</span></span>
<span data-ttu-id="aa706-133">passthru</span><span class="sxs-lookup"><span data-stu-id="aa706-133">passthru</span></span>

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

### <span data-ttu-id="aa706-134">-Password</span><span class="sxs-lookup"><span data-stu-id="aa706-134">-Password</span></span>
<span data-ttu-id="aa706-135">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="aa706-135">Specifies the user password.</span></span>
<span data-ttu-id="aa706-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="aa706-136">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa706-137">-State</span><span class="sxs-lookup"><span data-stu-id="aa706-137">-State</span></span>
<span data-ttu-id="aa706-138">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="aa706-138">Specifies the user state.</span></span>
<span data-ttu-id="aa706-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="aa706-139">This parameter is optional.</span></span>
<span data-ttu-id="aa706-140">預設值為 [作用中]。</span><span class="sxs-lookup"><span data-stu-id="aa706-140">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa706-141">-UserId</span><span class="sxs-lookup"><span data-stu-id="aa706-141">-UserId</span></span>
<span data-ttu-id="aa706-142">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa706-142">Specifies the user ID.</span></span>
<span data-ttu-id="aa706-143">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="aa706-143">This parameter is required.</span></span>

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

### <span data-ttu-id="aa706-144">-確認</span><span class="sxs-lookup"><span data-stu-id="aa706-144">-Confirm</span></span>
<span data-ttu-id="aa706-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa706-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa706-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa706-146">-WhatIf</span></span>
<span data-ttu-id="aa706-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa706-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa706-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa706-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa706-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa706-149">CommonParameters</span></span>
<span data-ttu-id="aa706-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa706-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa706-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aa706-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa706-152">輸入</span><span class="sxs-lookup"><span data-stu-id="aa706-152">INPUTS</span></span>

### <span data-ttu-id="aa706-153">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="aa706-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa706-154">System.object</span><span class="sxs-lookup"><span data-stu-id="aa706-154">System.String</span></span>

### <span data-ttu-id="aa706-155">SecureString</span><span class="sxs-lookup"><span data-stu-id="aa706-155">System.Security.SecureString</span></span>

### <span data-ttu-id="aa706-156">ServiceManagement. PsApiManagementUserState （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="aa706-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="aa706-157">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="aa706-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa706-158">輸出</span><span class="sxs-lookup"><span data-stu-id="aa706-158">OUTPUTS</span></span>

### <span data-ttu-id="aa706-159">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="aa706-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="aa706-160">筆記</span><span class="sxs-lookup"><span data-stu-id="aa706-160">NOTES</span></span>

## <span data-ttu-id="aa706-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa706-161">RELATED LINKS</span></span>

[<span data-ttu-id="aa706-162">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aa706-162">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="aa706-163">新-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aa706-163">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="aa706-164">移除-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aa706-164">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

