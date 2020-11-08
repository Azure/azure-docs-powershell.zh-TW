---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: a70cc953da853fd07dcee835f5a97a0efd2f6406
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965614"
---
# <span data-ttu-id="7dc40-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7dc40-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="7dc40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dc40-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc40-103">設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7dc40-103">Sets user details.</span></span>

## <span data-ttu-id="7dc40-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dc40-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dc40-105">說明</span><span class="sxs-lookup"><span data-stu-id="7dc40-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc40-106">**AzApiManagementUser** Cmdlet 會設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7dc40-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="7dc40-107">示例</span><span class="sxs-lookup"><span data-stu-id="7dc40-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc40-108">範例1：變更使用者的密碼、電子郵件地址及狀態</span><span class="sxs-lookup"><span data-stu-id="7dc40-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="7dc40-109">這個命令會設定新的使用者密碼和電子郵件地址，並封鎖使用者。</span><span class="sxs-lookup"><span data-stu-id="7dc40-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="7dc40-110">參數</span><span class="sxs-lookup"><span data-stu-id="7dc40-110">PARAMETERS</span></span>

### <span data-ttu-id="7dc40-111">-內容</span><span class="sxs-lookup"><span data-stu-id="7dc40-111">-Context</span></span>
<span data-ttu-id="7dc40-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dc40-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7dc40-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7dc40-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7dc40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc40-114">-DefaultProfile</span></span>
<span data-ttu-id="7dc40-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dc40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc40-116">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="7dc40-116">-Email</span></span>
<span data-ttu-id="7dc40-117">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="7dc40-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="7dc40-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7dc40-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7dc40-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7dc40-119">-FirstName</span></span>
<span data-ttu-id="7dc40-120">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="7dc40-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="7dc40-121">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="7dc40-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="7dc40-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="7dc40-122">-LastName</span></span>
<span data-ttu-id="7dc40-123">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="7dc40-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="7dc40-124">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="7dc40-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="7dc40-125">-記事</span><span class="sxs-lookup"><span data-stu-id="7dc40-125">-Note</span></span>
<span data-ttu-id="7dc40-126">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="7dc40-126">Specifies a note about the user.</span></span>
<span data-ttu-id="7dc40-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7dc40-127">This parameter is optional.</span></span>
<span data-ttu-id="7dc40-128">此參數的預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="7dc40-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="7dc40-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dc40-129">-PassThru</span></span>
<span data-ttu-id="7dc40-130">passthru</span><span class="sxs-lookup"><span data-stu-id="7dc40-130">passthru</span></span>

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

### <span data-ttu-id="7dc40-131">-Password</span><span class="sxs-lookup"><span data-stu-id="7dc40-131">-Password</span></span>
<span data-ttu-id="7dc40-132">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="7dc40-132">Specifies the user password.</span></span>
<span data-ttu-id="7dc40-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7dc40-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="7dc40-134">-State</span><span class="sxs-lookup"><span data-stu-id="7dc40-134">-State</span></span>
<span data-ttu-id="7dc40-135">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="7dc40-135">Specifies the user state.</span></span>
<span data-ttu-id="7dc40-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7dc40-136">This parameter is optional.</span></span>
<span data-ttu-id="7dc40-137">預設值為 [作用中]。</span><span class="sxs-lookup"><span data-stu-id="7dc40-137">The default value is Active.</span></span>

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

### <span data-ttu-id="7dc40-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="7dc40-138">-UserId</span></span>
<span data-ttu-id="7dc40-139">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7dc40-139">Specifies the user ID.</span></span>
<span data-ttu-id="7dc40-140">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7dc40-140">This parameter is required.</span></span>

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

### <span data-ttu-id="7dc40-141">-確認</span><span class="sxs-lookup"><span data-stu-id="7dc40-141">-Confirm</span></span>
<span data-ttu-id="7dc40-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7dc40-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dc40-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dc40-143">-WhatIf</span></span>
<span data-ttu-id="7dc40-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7dc40-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dc40-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dc40-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dc40-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc40-146">CommonParameters</span></span>
<span data-ttu-id="7dc40-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dc40-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc40-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7dc40-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc40-149">輸入</span><span class="sxs-lookup"><span data-stu-id="7dc40-149">INPUTS</span></span>

### <span data-ttu-id="7dc40-150">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7dc40-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7dc40-151">System.object</span><span class="sxs-lookup"><span data-stu-id="7dc40-151">System.String</span></span>

### <span data-ttu-id="7dc40-152">SecureString</span><span class="sxs-lookup"><span data-stu-id="7dc40-152">System.Security.SecureString</span></span>

### <span data-ttu-id="7dc40-153">ServiceManagement. PsApiManagementUserState （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7dc40-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="7dc40-154">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7dc40-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7dc40-155">輸出</span><span class="sxs-lookup"><span data-stu-id="7dc40-155">OUTPUTS</span></span>

### <span data-ttu-id="7dc40-156">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7dc40-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="7dc40-157">筆記</span><span class="sxs-lookup"><span data-stu-id="7dc40-157">NOTES</span></span>

## <span data-ttu-id="7dc40-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dc40-158">RELATED LINKS</span></span>

[<span data-ttu-id="7dc40-159">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7dc40-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="7dc40-160">新-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7dc40-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="7dc40-161">移除-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7dc40-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

