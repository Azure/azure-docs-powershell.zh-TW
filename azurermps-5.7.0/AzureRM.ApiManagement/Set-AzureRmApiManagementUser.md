---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455551"
---
# <span data-ttu-id="48aa2-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="48aa2-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="48aa2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="48aa2-103">設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="48aa2-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48aa2-104">句法</span><span class="sxs-lookup"><span data-stu-id="48aa2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48aa2-105">說明</span><span class="sxs-lookup"><span data-stu-id="48aa2-105">DESCRIPTION</span></span>
<span data-ttu-id="48aa2-106">**AzureRmApiManagementUser** Cmdlet 會設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="48aa2-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="48aa2-107">示例</span><span class="sxs-lookup"><span data-stu-id="48aa2-107">EXAMPLES</span></span>

### <span data-ttu-id="48aa2-108">範例1：變更使用者的密碼、電子郵件地址及狀態</span><span class="sxs-lookup"><span data-stu-id="48aa2-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="48aa2-109">這個命令會設定新的使用者密碼和電子郵件地址，並封鎖使用者。</span><span class="sxs-lookup"><span data-stu-id="48aa2-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="48aa2-110">參數</span><span class="sxs-lookup"><span data-stu-id="48aa2-110">PARAMETERS</span></span>

### <span data-ttu-id="48aa2-111">-內容</span><span class="sxs-lookup"><span data-stu-id="48aa2-111">-Context</span></span>
<span data-ttu-id="48aa2-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="48aa2-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="48aa2-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="48aa2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="48aa2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48aa2-114">-DefaultProfile</span></span>
<span data-ttu-id="48aa2-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48aa2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="48aa2-116">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="48aa2-116">-Email</span></span>
<span data-ttu-id="48aa2-117">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="48aa2-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="48aa2-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="48aa2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="48aa2-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="48aa2-119">-FirstName</span></span>
<span data-ttu-id="48aa2-120">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="48aa2-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="48aa2-121">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="48aa2-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="48aa2-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="48aa2-122">-LastName</span></span>
<span data-ttu-id="48aa2-123">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="48aa2-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="48aa2-124">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="48aa2-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="48aa2-125">-記事</span><span class="sxs-lookup"><span data-stu-id="48aa2-125">-Note</span></span>
<span data-ttu-id="48aa2-126">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="48aa2-126">Specifies a note about the user.</span></span>
<span data-ttu-id="48aa2-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="48aa2-127">This parameter is optional.</span></span>
<span data-ttu-id="48aa2-128">此參數的預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="48aa2-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="48aa2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48aa2-129">-PassThru</span></span>
<span data-ttu-id="48aa2-130">passthru</span><span class="sxs-lookup"><span data-stu-id="48aa2-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48aa2-131">-Password</span><span class="sxs-lookup"><span data-stu-id="48aa2-131">-Password</span></span>
<span data-ttu-id="48aa2-132">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="48aa2-132">Specifies the user password.</span></span>
<span data-ttu-id="48aa2-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="48aa2-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48aa2-134">-State</span><span class="sxs-lookup"><span data-stu-id="48aa2-134">-State</span></span>
<span data-ttu-id="48aa2-135">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="48aa2-135">Specifies the user state.</span></span>
<span data-ttu-id="48aa2-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="48aa2-136">This parameter is optional.</span></span>
<span data-ttu-id="48aa2-137">預設值為 [作用中]。</span><span class="sxs-lookup"><span data-stu-id="48aa2-137">The default value is Active.</span></span>

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

### <span data-ttu-id="48aa2-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="48aa2-138">-UserId</span></span>
<span data-ttu-id="48aa2-139">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="48aa2-139">Specifies the user ID.</span></span>
<span data-ttu-id="48aa2-140">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="48aa2-140">This parameter is required.</span></span>

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

### <span data-ttu-id="48aa2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48aa2-141">CommonParameters</span></span>
<span data-ttu-id="48aa2-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48aa2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48aa2-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48aa2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48aa2-144">輸入</span><span class="sxs-lookup"><span data-stu-id="48aa2-144">INPUTS</span></span>

### <span data-ttu-id="48aa2-145">所有</span><span class="sxs-lookup"><span data-stu-id="48aa2-145">None</span></span>
<span data-ttu-id="48aa2-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="48aa2-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48aa2-147">輸出</span><span class="sxs-lookup"><span data-stu-id="48aa2-147">OUTPUTS</span></span>

### <span data-ttu-id="48aa2-148">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="48aa2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="48aa2-149">筆記</span><span class="sxs-lookup"><span data-stu-id="48aa2-149">NOTES</span></span>

## <span data-ttu-id="48aa2-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="48aa2-150">RELATED LINKS</span></span>

[<span data-ttu-id="48aa2-151">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="48aa2-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="48aa2-152">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="48aa2-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="48aa2-153">移除-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="48aa2-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


