---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626575"
---
# <span data-ttu-id="153fc-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="153fc-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="153fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="153fc-102">SYNOPSIS</span></span>
<span data-ttu-id="153fc-103">註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="153fc-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="153fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="153fc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="153fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="153fc-105">DESCRIPTION</span></span>
<span data-ttu-id="153fc-106">**新的-AzureRmApiManagementUser** Cmdlet 會註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="153fc-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="153fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="153fc-107">EXAMPLES</span></span>

### <span data-ttu-id="153fc-108">範例1：註冊新的使用者</span><span class="sxs-lookup"><span data-stu-id="153fc-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="153fc-109">這個命令會將一個名為 Patti 的新使用者更完整。</span><span class="sxs-lookup"><span data-stu-id="153fc-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="153fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="153fc-110">PARAMETERS</span></span>

### <span data-ttu-id="153fc-111">-內容</span><span class="sxs-lookup"><span data-stu-id="153fc-111">-Context</span></span>
<span data-ttu-id="153fc-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="153fc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="153fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153fc-113">-DefaultProfile</span></span>
<span data-ttu-id="153fc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="153fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="153fc-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="153fc-115">-Email</span></span>
<span data-ttu-id="153fc-116">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="153fc-116">Specifies the email address of the user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="153fc-117">-FirstName</span></span>
<span data-ttu-id="153fc-118">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="153fc-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="153fc-119">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="153fc-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="153fc-120">-LastName</span></span>
<span data-ttu-id="153fc-121">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="153fc-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="153fc-122">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="153fc-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-123">-記事</span><span class="sxs-lookup"><span data-stu-id="153fc-123">-Note</span></span>
<span data-ttu-id="153fc-124">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="153fc-124">Specifies a note about the user.</span></span>
<span data-ttu-id="153fc-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="153fc-125">This parameter is optional.</span></span>
<span data-ttu-id="153fc-126">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="153fc-126">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-127">-Password</span><span class="sxs-lookup"><span data-stu-id="153fc-127">-Password</span></span>
<span data-ttu-id="153fc-128">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="153fc-128">Specifies the user password.</span></span>
<span data-ttu-id="153fc-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="153fc-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-130">-State</span><span class="sxs-lookup"><span data-stu-id="153fc-130">-State</span></span>
<span data-ttu-id="153fc-131">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="153fc-131">Specifies the user state.</span></span>
<span data-ttu-id="153fc-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="153fc-132">This parameter is optional.</span></span>
<span data-ttu-id="153fc-133">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="153fc-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="153fc-134">-UserId</span></span>
<span data-ttu-id="153fc-135">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="153fc-135">Specifies the user ID.</span></span>
<span data-ttu-id="153fc-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="153fc-136">This parameter is optional.</span></span>
<span data-ttu-id="153fc-137">如果未指定此參數，此 Cmdlet 會產生使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="153fc-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153fc-138">CommonParameters</span></span>
<span data-ttu-id="153fc-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="153fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153fc-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="153fc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153fc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="153fc-141">INPUTS</span></span>

### <span data-ttu-id="153fc-142">所有</span><span class="sxs-lookup"><span data-stu-id="153fc-142">None</span></span>
<span data-ttu-id="153fc-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="153fc-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="153fc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="153fc-144">OUTPUTS</span></span>

### <span data-ttu-id="153fc-145">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="153fc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="153fc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="153fc-146">NOTES</span></span>

## <span data-ttu-id="153fc-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="153fc-147">RELATED LINKS</span></span>

[<span data-ttu-id="153fc-148">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="153fc-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="153fc-149">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="153fc-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


