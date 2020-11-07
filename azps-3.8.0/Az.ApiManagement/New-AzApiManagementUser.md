---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958149"
---
# <span data-ttu-id="5a156-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5a156-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="5a156-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a156-102">SYNOPSIS</span></span>
<span data-ttu-id="5a156-103">註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="5a156-103">Registers a new user.</span></span>

## <span data-ttu-id="5a156-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a156-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a156-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a156-105">DESCRIPTION</span></span>
<span data-ttu-id="5a156-106">**新的-AzApiManagementUser** Cmdlet 會註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="5a156-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="5a156-107">示例</span><span class="sxs-lookup"><span data-stu-id="5a156-107">EXAMPLES</span></span>

### <span data-ttu-id="5a156-108">範例1：註冊新的使用者</span><span class="sxs-lookup"><span data-stu-id="5a156-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="5a156-109">這個命令會將一個名為 Patti 的新使用者更完整。</span><span class="sxs-lookup"><span data-stu-id="5a156-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="5a156-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a156-110">PARAMETERS</span></span>

### <span data-ttu-id="5a156-111">-內容</span><span class="sxs-lookup"><span data-stu-id="5a156-111">-Context</span></span>
<span data-ttu-id="5a156-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="5a156-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a156-113">-DefaultProfile</span></span>
<span data-ttu-id="5a156-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a156-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a156-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="5a156-115">-Email</span></span>
<span data-ttu-id="5a156-116">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="5a156-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="5a156-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="5a156-117">-FirstName</span></span>
<span data-ttu-id="5a156-118">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="5a156-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="5a156-119">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="5a156-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="5a156-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="5a156-120">-LastName</span></span>
<span data-ttu-id="5a156-121">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="5a156-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="5a156-122">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="5a156-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="5a156-123">-記事</span><span class="sxs-lookup"><span data-stu-id="5a156-123">-Note</span></span>
<span data-ttu-id="5a156-124">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="5a156-124">Specifies a note about the user.</span></span>
<span data-ttu-id="5a156-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="5a156-125">This parameter is optional.</span></span>
<span data-ttu-id="5a156-126">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="5a156-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="5a156-127">-Password</span><span class="sxs-lookup"><span data-stu-id="5a156-127">-Password</span></span>
<span data-ttu-id="5a156-128">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="5a156-128">Specifies the user password.</span></span>
<span data-ttu-id="5a156-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5a156-129">This parameter is required.</span></span>

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

### <span data-ttu-id="5a156-130">-State</span><span class="sxs-lookup"><span data-stu-id="5a156-130">-State</span></span>
<span data-ttu-id="5a156-131">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="5a156-131">Specifies the user state.</span></span>
<span data-ttu-id="5a156-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="5a156-132">This parameter is optional.</span></span>
<span data-ttu-id="5a156-133">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="5a156-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5a156-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="5a156-134">-UserId</span></span>
<span data-ttu-id="5a156-135">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a156-135">Specifies the user ID.</span></span>
<span data-ttu-id="5a156-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="5a156-136">This parameter is optional.</span></span>
<span data-ttu-id="5a156-137">如果未指定此參數，此 Cmdlet 會產生使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a156-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="5a156-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a156-138">CommonParameters</span></span>
<span data-ttu-id="5a156-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a156-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a156-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a156-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a156-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5a156-141">INPUTS</span></span>

### <span data-ttu-id="5a156-142">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5a156-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a156-143">System.object</span><span class="sxs-lookup"><span data-stu-id="5a156-143">System.String</span></span>

### <span data-ttu-id="5a156-144">SecureString</span><span class="sxs-lookup"><span data-stu-id="5a156-144">System.Security.SecureString</span></span>

### <span data-ttu-id="5a156-145">ApiManagement 為 Nullable "1 [PsApiManagementUserState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="5a156-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5a156-146">輸出</span><span class="sxs-lookup"><span data-stu-id="5a156-146">OUTPUTS</span></span>

### <span data-ttu-id="5a156-147">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5a156-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="5a156-148">筆記</span><span class="sxs-lookup"><span data-stu-id="5a156-148">NOTES</span></span>

## <span data-ttu-id="5a156-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a156-149">RELATED LINKS</span></span>

[<span data-ttu-id="5a156-150">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5a156-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="5a156-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5a156-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


