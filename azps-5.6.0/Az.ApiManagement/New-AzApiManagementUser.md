---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903717"
---
# <span data-ttu-id="74104-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74104-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="74104-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74104-102">SYNOPSIS</span></span>
<span data-ttu-id="74104-103">註冊新使用者。</span><span class="sxs-lookup"><span data-stu-id="74104-103">Registers a new user.</span></span>

## <span data-ttu-id="74104-104">語法</span><span class="sxs-lookup"><span data-stu-id="74104-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74104-105">描述</span><span class="sxs-lookup"><span data-stu-id="74104-105">DESCRIPTION</span></span>
<span data-ttu-id="74104-106">**New-AzApiManagementUser** Cmdlet 會註冊新使用者。</span><span class="sxs-lookup"><span data-stu-id="74104-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="74104-107">例子</span><span class="sxs-lookup"><span data-stu-id="74104-107">EXAMPLES</span></span>

### <span data-ttu-id="74104-108">範例 1：註冊新使用者</span><span class="sxs-lookup"><span data-stu-id="74104-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="74104-109">此命令會註冊一個名為帕提 Fuller 的新使用者。</span><span class="sxs-lookup"><span data-stu-id="74104-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="74104-110">參數</span><span class="sxs-lookup"><span data-stu-id="74104-110">PARAMETERS</span></span>

### <span data-ttu-id="74104-111">-內容</span><span class="sxs-lookup"><span data-stu-id="74104-111">-Context</span></span>
<span data-ttu-id="74104-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="74104-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="74104-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74104-113">-DefaultProfile</span></span>
<span data-ttu-id="74104-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74104-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74104-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="74104-115">-Email</span></span>
<span data-ttu-id="74104-116">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="74104-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="74104-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="74104-117">-FirstName</span></span>
<span data-ttu-id="74104-118">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="74104-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="74104-119">此參數必須長 1 到 100 個字元。</span><span class="sxs-lookup"><span data-stu-id="74104-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="74104-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="74104-120">-LastName</span></span>
<span data-ttu-id="74104-121">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="74104-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="74104-122">此參數必須長 1 到 100 個字元。</span><span class="sxs-lookup"><span data-stu-id="74104-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="74104-123">-注意</span><span class="sxs-lookup"><span data-stu-id="74104-123">-Note</span></span>
<span data-ttu-id="74104-124">指定關於使用者的附注。</span><span class="sxs-lookup"><span data-stu-id="74104-124">Specifies a note about the user.</span></span>
<span data-ttu-id="74104-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="74104-125">This parameter is optional.</span></span>
<span data-ttu-id="74104-126">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="74104-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="74104-127">-密碼</span><span class="sxs-lookup"><span data-stu-id="74104-127">-Password</span></span>
<span data-ttu-id="74104-128">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="74104-128">Specifies the user password.</span></span>
<span data-ttu-id="74104-129">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="74104-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74104-130">-State</span><span class="sxs-lookup"><span data-stu-id="74104-130">-State</span></span>
<span data-ttu-id="74104-131">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="74104-131">Specifies the user state.</span></span>
<span data-ttu-id="74104-132">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="74104-132">This parameter is optional.</span></span>
<span data-ttu-id="74104-133">此參數的預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="74104-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74104-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="74104-134">-UserId</span></span>
<span data-ttu-id="74104-135">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="74104-135">Specifies the user ID.</span></span>
<span data-ttu-id="74104-136">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="74104-136">This parameter is optional.</span></span>
<span data-ttu-id="74104-137">如果未指定此參數，此 Cmdlet 會產生使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="74104-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="74104-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74104-138">CommonParameters</span></span>
<span data-ttu-id="74104-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74104-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74104-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74104-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74104-141">輸入</span><span class="sxs-lookup"><span data-stu-id="74104-141">INPUTS</span></span>

### <span data-ttu-id="74104-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="74104-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74104-143">System.String</span><span class="sxs-lookup"><span data-stu-id="74104-143">System.String</span></span>

### <span data-ttu-id="74104-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="74104-144">System.Security.SecureString</span></span>

### <span data-ttu-id="74104-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="74104-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="74104-146">輸出</span><span class="sxs-lookup"><span data-stu-id="74104-146">OUTPUTS</span></span>

### <span data-ttu-id="74104-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74104-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="74104-148">筆記</span><span class="sxs-lookup"><span data-stu-id="74104-148">NOTES</span></span>

## <span data-ttu-id="74104-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="74104-149">RELATED LINKS</span></span>

[<span data-ttu-id="74104-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74104-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="74104-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74104-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


