---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623943"
---
# <span data-ttu-id="1e8c8-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1e8c8-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="1e8c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8c8-103">註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e8c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e8c8-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e8c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8c8-106">**新的-AzureRmApiManagementUser** Cmdlet 會註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="1e8c8-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e8c8-107">EXAMPLES</span></span>

### <span data-ttu-id="1e8c8-108">範例1：註冊新的使用者</span><span class="sxs-lookup"><span data-stu-id="1e8c8-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="1e8c8-109">這個命令會將一個名為 Patti 的新使用者更完整。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="1e8c8-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e8c8-110">PARAMETERS</span></span>

### <span data-ttu-id="1e8c8-111">-內容</span><span class="sxs-lookup"><span data-stu-id="1e8c8-111">-Context</span></span>
<span data-ttu-id="1e8c8-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1e8c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8c8-113">-DefaultProfile</span></span>
<span data-ttu-id="1e8c8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e8c8-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="1e8c8-115">-Email</span></span>
<span data-ttu-id="1e8c8-116">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="1e8c8-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1e8c8-117">-FirstName</span></span>
<span data-ttu-id="1e8c8-118">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="1e8c8-119">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1e8c8-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="1e8c8-120">-LastName</span></span>
<span data-ttu-id="1e8c8-121">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="1e8c8-122">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1e8c8-123">-記事</span><span class="sxs-lookup"><span data-stu-id="1e8c8-123">-Note</span></span>
<span data-ttu-id="1e8c8-124">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-124">Specifies a note about the user.</span></span>
<span data-ttu-id="1e8c8-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-125">This parameter is optional.</span></span>
<span data-ttu-id="1e8c8-126">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="1e8c8-127">-Password</span><span class="sxs-lookup"><span data-stu-id="1e8c8-127">-Password</span></span>
<span data-ttu-id="1e8c8-128">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-128">Specifies the user password.</span></span>
<span data-ttu-id="1e8c8-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-129">This parameter is required.</span></span>

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

### <span data-ttu-id="1e8c8-130">-State</span><span class="sxs-lookup"><span data-stu-id="1e8c8-130">-State</span></span>
<span data-ttu-id="1e8c8-131">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-131">Specifies the user state.</span></span>
<span data-ttu-id="1e8c8-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-132">This parameter is optional.</span></span>
<span data-ttu-id="1e8c8-133">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1e8c8-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="1e8c8-134">-UserId</span></span>
<span data-ttu-id="1e8c8-135">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-135">Specifies the user ID.</span></span>
<span data-ttu-id="1e8c8-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-136">This parameter is optional.</span></span>
<span data-ttu-id="1e8c8-137">如果未指定此參數，此 Cmdlet 會產生使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="1e8c8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8c8-138">CommonParameters</span></span>
<span data-ttu-id="1e8c8-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8c8-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8c8-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1e8c8-141">INPUTS</span></span>

### <span data-ttu-id="1e8c8-142">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1e8c8-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1e8c8-143">System.object</span><span class="sxs-lookup"><span data-stu-id="1e8c8-143">System.String</span></span>

### <span data-ttu-id="1e8c8-144">SecureString</span><span class="sxs-lookup"><span data-stu-id="1e8c8-144">System.Security.SecureString</span></span>

### <span data-ttu-id="1e8c8-145">ApiManagement 為 Nullable "1 [PsApiManagementUserState，，，ServiceManagement，Version = ServiceManagement，Culture = 中性，PublicKeyToken = null]]。））。</span><span class="sxs-lookup"><span data-stu-id="1e8c8-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1e8c8-146">輸出</span><span class="sxs-lookup"><span data-stu-id="1e8c8-146">OUTPUTS</span></span>

### <span data-ttu-id="1e8c8-147">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1e8c8-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1e8c8-148">筆記</span><span class="sxs-lookup"><span data-stu-id="1e8c8-148">NOTES</span></span>

## <span data-ttu-id="1e8c8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e8c8-149">RELATED LINKS</span></span>

[<span data-ttu-id="1e8c8-150">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1e8c8-150">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="1e8c8-151">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1e8c8-151">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


