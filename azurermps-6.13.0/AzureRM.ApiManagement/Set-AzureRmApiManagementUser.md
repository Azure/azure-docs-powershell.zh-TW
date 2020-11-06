---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445784"
---
# <span data-ttu-id="7401e-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7401e-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="7401e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7401e-102">SYNOPSIS</span></span>
<span data-ttu-id="7401e-103">設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7401e-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7401e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7401e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7401e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7401e-105">DESCRIPTION</span></span>
<span data-ttu-id="7401e-106">**AzureRmApiManagementUser** Cmdlet 會設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7401e-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="7401e-107">示例</span><span class="sxs-lookup"><span data-stu-id="7401e-107">EXAMPLES</span></span>

### <span data-ttu-id="7401e-108">範例1：變更使用者的密碼、電子郵件地址及狀態</span><span class="sxs-lookup"><span data-stu-id="7401e-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="7401e-109">這個命令會設定新的使用者密碼和電子郵件地址，並封鎖使用者。</span><span class="sxs-lookup"><span data-stu-id="7401e-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="7401e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7401e-110">PARAMETERS</span></span>

### <span data-ttu-id="7401e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="7401e-111">-Context</span></span>
<span data-ttu-id="7401e-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="7401e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7401e-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7401e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7401e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7401e-114">-DefaultProfile</span></span>
<span data-ttu-id="7401e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7401e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7401e-116">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="7401e-116">-Email</span></span>
<span data-ttu-id="7401e-117">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="7401e-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="7401e-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7401e-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7401e-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7401e-119">-FirstName</span></span>
<span data-ttu-id="7401e-120">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="7401e-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="7401e-121">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="7401e-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="7401e-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="7401e-122">-LastName</span></span>
<span data-ttu-id="7401e-123">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="7401e-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="7401e-124">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="7401e-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="7401e-125">-記事</span><span class="sxs-lookup"><span data-stu-id="7401e-125">-Note</span></span>
<span data-ttu-id="7401e-126">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="7401e-126">Specifies a note about the user.</span></span>
<span data-ttu-id="7401e-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7401e-127">This parameter is optional.</span></span>
<span data-ttu-id="7401e-128">此參數的預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="7401e-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="7401e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7401e-129">-PassThru</span></span>
<span data-ttu-id="7401e-130">passthru</span><span class="sxs-lookup"><span data-stu-id="7401e-130">passthru</span></span>

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

### <span data-ttu-id="7401e-131">-Password</span><span class="sxs-lookup"><span data-stu-id="7401e-131">-Password</span></span>
<span data-ttu-id="7401e-132">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="7401e-132">Specifies the user password.</span></span>
<span data-ttu-id="7401e-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7401e-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="7401e-134">-State</span><span class="sxs-lookup"><span data-stu-id="7401e-134">-State</span></span>
<span data-ttu-id="7401e-135">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="7401e-135">Specifies the user state.</span></span>
<span data-ttu-id="7401e-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7401e-136">This parameter is optional.</span></span>
<span data-ttu-id="7401e-137">預設值為 [作用中]。</span><span class="sxs-lookup"><span data-stu-id="7401e-137">The default value is Active.</span></span>

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

### <span data-ttu-id="7401e-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="7401e-138">-UserId</span></span>
<span data-ttu-id="7401e-139">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7401e-139">Specifies the user ID.</span></span>
<span data-ttu-id="7401e-140">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7401e-140">This parameter is required.</span></span>

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

### <span data-ttu-id="7401e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7401e-141">CommonParameters</span></span>
<span data-ttu-id="7401e-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7401e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7401e-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7401e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7401e-144">輸入</span><span class="sxs-lookup"><span data-stu-id="7401e-144">INPUTS</span></span>

### <span data-ttu-id="7401e-145">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7401e-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7401e-146">System.object</span><span class="sxs-lookup"><span data-stu-id="7401e-146">System.String</span></span>

### <span data-ttu-id="7401e-147">SecureString</span><span class="sxs-lookup"><span data-stu-id="7401e-147">System.Security.SecureString</span></span>

### <span data-ttu-id="7401e-148">ServiceManagement. PsApiManagementUserState （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7401e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="7401e-149">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7401e-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7401e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="7401e-150">OUTPUTS</span></span>

### <span data-ttu-id="7401e-151">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7401e-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="7401e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="7401e-152">NOTES</span></span>

## <span data-ttu-id="7401e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="7401e-153">RELATED LINKS</span></span>

[<span data-ttu-id="7401e-154">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7401e-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="7401e-155">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7401e-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="7401e-156">移除-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7401e-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


