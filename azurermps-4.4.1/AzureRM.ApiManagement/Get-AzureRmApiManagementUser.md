---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445216"
---
# <span data-ttu-id="40b3d-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40b3d-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="40b3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="40b3d-103">取得使用者或使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="40b3d-104">SYNTAX</span></span>

### <span data-ttu-id="40b3d-105"> (預設) 取得所有使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40b3d-106">透過識別碼取得使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b3d-107">尋找使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b3d-108">說明</span><span class="sxs-lookup"><span data-stu-id="40b3d-108">DESCRIPTION</span></span>
<span data-ttu-id="40b3d-109">如果沒有指定使用者， **AzureRmApiManagementUser** Cmdlet 會取得指定的使用者或所有使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="40b3d-110">示例</span><span class="sxs-lookup"><span data-stu-id="40b3d-110">EXAMPLES</span></span>

### <span data-ttu-id="40b3d-111">範例1：取得所有使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="40b3d-112">這個命令會取得所有使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-112">This command gets all users.</span></span>

### <span data-ttu-id="40b3d-113">範例2：依識別碼取得使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="40b3d-114">這個命令會透過識別碼取得使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="40b3d-115">範例：依姓氏取得使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="40b3d-116">這個命令會取得擁有指定姓氏的使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="40b3d-117">範例4：透過電子郵件地址取得使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="40b3d-118">這個命令會取得擁有指定電子郵件地址的使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="40b3d-119">範例5：取得群組中的所有使用者</span><span class="sxs-lookup"><span data-stu-id="40b3d-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="40b3d-120">這個命令會取得指定群組中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="40b3d-121">參數</span><span class="sxs-lookup"><span data-stu-id="40b3d-121">PARAMETERS</span></span>

### <span data-ttu-id="40b3d-122">-內容</span><span class="sxs-lookup"><span data-stu-id="40b3d-122">-Context</span></span>
<span data-ttu-id="40b3d-123">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="40b3d-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="40b3d-124">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="40b3d-124">-Email</span></span>
<span data-ttu-id="40b3d-125">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="40b3d-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="40b3d-126">如果指定此參數，此 Cmdlet 會透過電子郵件尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="40b3d-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40b3d-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b3d-128">-FirstName</span><span class="sxs-lookup"><span data-stu-id="40b3d-128">-FirstName</span></span>
<span data-ttu-id="40b3d-129">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="40b3d-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="40b3d-130">如果指定此參數，這個 Cmdlet 會依名字尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="40b3d-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40b3d-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b3d-132">-GroupId</span><span class="sxs-lookup"><span data-stu-id="40b3d-132">-GroupId</span></span>
<span data-ttu-id="40b3d-133">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="40b3d-133">Specifies the group identifier.</span></span>
<span data-ttu-id="40b3d-134">如果已指定，此 Cmdlet 會找出指定群組中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="40b3d-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40b3d-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b3d-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="40b3d-136">-LastName</span></span>
<span data-ttu-id="40b3d-137">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="40b3d-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="40b3d-138">如果已指定，此 Cmdlet 會依姓氏尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="40b3d-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40b3d-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b3d-140">-State</span><span class="sxs-lookup"><span data-stu-id="40b3d-140">-State</span></span>
<span data-ttu-id="40b3d-141">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="40b3d-141">Specifies the user state.</span></span>
<span data-ttu-id="40b3d-142">如果已指定，此 Cmdlet 會尋找處於這種狀態的使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="40b3d-143">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40b3d-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b3d-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="40b3d-144">-UserId</span></span>
<span data-ttu-id="40b3d-145">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="40b3d-145">Specifies a user ID.</span></span>
<span data-ttu-id="40b3d-146">如果已指定，此 Cmdlet 會依據此識別碼來尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="40b3d-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="40b3d-147">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40b3d-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b3d-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b3d-148">-DefaultProfile</span></span>
<span data-ttu-id="40b3d-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40b3d-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b3d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b3d-150">CommonParameters</span></span>
<span data-ttu-id="40b3d-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40b3d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b3d-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40b3d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b3d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="40b3d-153">INPUTS</span></span>

## <span data-ttu-id="40b3d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="40b3d-154">OUTPUTS</span></span>

### <span data-ttu-id="40b3d-155">IList<ApiManagement. ServiceManagement. PsApiManagementUser]></span><span class="sxs-lookup"><span data-stu-id="40b3d-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="40b3d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="40b3d-156">NOTES</span></span>

## <span data-ttu-id="40b3d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="40b3d-157">RELATED LINKS</span></span>

[<span data-ttu-id="40b3d-158">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40b3d-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="40b3d-159">移除-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40b3d-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="40b3d-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40b3d-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


