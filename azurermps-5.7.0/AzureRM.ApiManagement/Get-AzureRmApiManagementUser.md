---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448795"
---
# <span data-ttu-id="9f5da-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9f5da-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="9f5da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f5da-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5da-103">取得使用者或使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f5da-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f5da-104">SYNTAX</span></span>

### <span data-ttu-id="9f5da-105">GeAllUsers (預設) </span><span class="sxs-lookup"><span data-stu-id="9f5da-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f5da-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="9f5da-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f5da-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="9f5da-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f5da-108">說明</span><span class="sxs-lookup"><span data-stu-id="9f5da-108">DESCRIPTION</span></span>
<span data-ttu-id="9f5da-109">如果沒有指定使用者， **AzureRmApiManagementUser** Cmdlet 會取得指定的使用者或所有使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="9f5da-110">示例</span><span class="sxs-lookup"><span data-stu-id="9f5da-110">EXAMPLES</span></span>

### <span data-ttu-id="9f5da-111">範例1：取得所有使用者</span><span class="sxs-lookup"><span data-stu-id="9f5da-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="9f5da-112">這個命令會取得所有使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-112">This command gets all users.</span></span>

### <span data-ttu-id="9f5da-113">範例2：依識別碼取得使用者</span><span class="sxs-lookup"><span data-stu-id="9f5da-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="9f5da-114">這個命令會透過識別碼取得使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="9f5da-115">範例：依姓氏取得使用者</span><span class="sxs-lookup"><span data-stu-id="9f5da-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="9f5da-116">這個命令會取得擁有指定姓氏的使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="9f5da-117">範例4：透過電子郵件地址取得使用者</span><span class="sxs-lookup"><span data-stu-id="9f5da-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="9f5da-118">這個命令會取得擁有指定電子郵件地址的使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="9f5da-119">範例5：取得群組中的所有使用者</span><span class="sxs-lookup"><span data-stu-id="9f5da-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="9f5da-120">這個命令會取得指定群組中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="9f5da-121">參數</span><span class="sxs-lookup"><span data-stu-id="9f5da-121">PARAMETERS</span></span>

### <span data-ttu-id="9f5da-122">-內容</span><span class="sxs-lookup"><span data-stu-id="9f5da-122">-Context</span></span>
<span data-ttu-id="9f5da-123">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="9f5da-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5da-124">-DefaultProfile</span></span>
<span data-ttu-id="9f5da-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f5da-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-126">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="9f5da-126">-Email</span></span>
<span data-ttu-id="9f5da-127">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9f5da-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="9f5da-128">如果指定此參數，此 Cmdlet 會透過電子郵件尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="9f5da-129">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f5da-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="9f5da-130">-FirstName</span></span>
<span data-ttu-id="9f5da-131">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="9f5da-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="9f5da-132">如果指定此參數，這個 Cmdlet 會依名字尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="9f5da-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f5da-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9f5da-134">-GroupId</span></span>
<span data-ttu-id="9f5da-135">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f5da-135">Specifies the group identifier.</span></span>
<span data-ttu-id="9f5da-136">如果已指定，此 Cmdlet 會找出指定群組中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="9f5da-137">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f5da-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="9f5da-138">-LastName</span></span>
<span data-ttu-id="9f5da-139">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="9f5da-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="9f5da-140">如果已指定，此 Cmdlet 會依姓氏尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="9f5da-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f5da-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-142">-State</span><span class="sxs-lookup"><span data-stu-id="9f5da-142">-State</span></span>
<span data-ttu-id="9f5da-143">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="9f5da-143">Specifies the user state.</span></span>
<span data-ttu-id="9f5da-144">如果已指定，此 Cmdlet 會尋找處於這種狀態的使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="9f5da-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f5da-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="9f5da-146">-UserId</span></span>
<span data-ttu-id="9f5da-147">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f5da-147">Specifies a user ID.</span></span>
<span data-ttu-id="9f5da-148">如果已指定，此 Cmdlet 會依據此識別碼來尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="9f5da-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="9f5da-149">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f5da-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5da-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5da-150">CommonParameters</span></span>
<span data-ttu-id="9f5da-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f5da-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5da-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f5da-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5da-153">輸入</span><span class="sxs-lookup"><span data-stu-id="9f5da-153">INPUTS</span></span>

### <span data-ttu-id="9f5da-154">所有</span><span class="sxs-lookup"><span data-stu-id="9f5da-154">None</span></span>
<span data-ttu-id="9f5da-155">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9f5da-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f5da-156">輸出</span><span class="sxs-lookup"><span data-stu-id="9f5da-156">OUTPUTS</span></span>

### <span data-ttu-id="9f5da-157">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9f5da-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="9f5da-158">API 管理服務中使用者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f5da-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="9f5da-159">IList<ApiManagement. ServiceManagement. PsApiManagementUser]></span><span class="sxs-lookup"><span data-stu-id="9f5da-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="9f5da-160">API 管理服務中的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="9f5da-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="9f5da-161">筆記</span><span class="sxs-lookup"><span data-stu-id="9f5da-161">NOTES</span></span>

## <span data-ttu-id="9f5da-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f5da-162">RELATED LINKS</span></span>

[<span data-ttu-id="9f5da-163">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9f5da-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="9f5da-164">移除-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9f5da-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="9f5da-165">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9f5da-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


