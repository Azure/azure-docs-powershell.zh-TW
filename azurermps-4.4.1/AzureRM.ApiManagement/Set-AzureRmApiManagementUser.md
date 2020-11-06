---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445163"
---
# <span data-ttu-id="926bc-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="926bc-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="926bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="926bc-102">SYNOPSIS</span></span>
<span data-ttu-id="926bc-103">設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="926bc-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="926bc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="926bc-105">DESCRIPTION</span></span>
<span data-ttu-id="926bc-106">**AzureRmApiManagementUser** Cmdlet 會設定使用者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="926bc-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="926bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="926bc-107">EXAMPLES</span></span>

### <span data-ttu-id="926bc-108">範例1：變更使用者的密碼、電子郵件地址及狀態</span><span class="sxs-lookup"><span data-stu-id="926bc-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="926bc-109">這個命令會設定新的使用者密碼和電子郵件地址，並封鎖使用者。</span><span class="sxs-lookup"><span data-stu-id="926bc-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="926bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="926bc-110">PARAMETERS</span></span>

### <span data-ttu-id="926bc-111">-內容</span><span class="sxs-lookup"><span data-stu-id="926bc-111">-Context</span></span>
<span data-ttu-id="926bc-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="926bc-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="926bc-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="926bc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="926bc-114">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="926bc-114">-Email</span></span>
<span data-ttu-id="926bc-115">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="926bc-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="926bc-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="926bc-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="926bc-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="926bc-117">-FirstName</span></span>
<span data-ttu-id="926bc-118">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="926bc-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="926bc-119">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="926bc-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="926bc-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="926bc-120">-LastName</span></span>
<span data-ttu-id="926bc-121">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="926bc-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="926bc-122">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="926bc-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="926bc-123">-記事</span><span class="sxs-lookup"><span data-stu-id="926bc-123">-Note</span></span>
<span data-ttu-id="926bc-124">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="926bc-124">Specifies a note about the user.</span></span>
<span data-ttu-id="926bc-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="926bc-125">This parameter is optional.</span></span>
<span data-ttu-id="926bc-126">此參數的預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="926bc-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="926bc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="926bc-127">-PassThru</span></span>
<span data-ttu-id="926bc-128">passthru</span><span class="sxs-lookup"><span data-stu-id="926bc-128">passthru</span></span>

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

### <span data-ttu-id="926bc-129">-Password</span><span class="sxs-lookup"><span data-stu-id="926bc-129">-Password</span></span>
<span data-ttu-id="926bc-130">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="926bc-130">Specifies the user password.</span></span>
<span data-ttu-id="926bc-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="926bc-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="926bc-132">-State</span><span class="sxs-lookup"><span data-stu-id="926bc-132">-State</span></span>
<span data-ttu-id="926bc-133">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="926bc-133">Specifies the user state.</span></span>
<span data-ttu-id="926bc-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="926bc-134">This parameter is optional.</span></span>
<span data-ttu-id="926bc-135">預設值為 [作用中]。</span><span class="sxs-lookup"><span data-stu-id="926bc-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="926bc-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="926bc-136">-UserId</span></span>
<span data-ttu-id="926bc-137">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="926bc-137">Specifies the user ID.</span></span>
<span data-ttu-id="926bc-138">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="926bc-138">This parameter is required.</span></span>

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

### <span data-ttu-id="926bc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926bc-139">-DefaultProfile</span></span>
<span data-ttu-id="926bc-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="926bc-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926bc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926bc-141">CommonParameters</span></span>
<span data-ttu-id="926bc-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="926bc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926bc-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="926bc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926bc-144">輸入</span><span class="sxs-lookup"><span data-stu-id="926bc-144">INPUTS</span></span>

## <span data-ttu-id="926bc-145">輸出</span><span class="sxs-lookup"><span data-stu-id="926bc-145">OUTPUTS</span></span>

### <span data-ttu-id="926bc-146">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="926bc-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="926bc-147">筆記</span><span class="sxs-lookup"><span data-stu-id="926bc-147">NOTES</span></span>

## <span data-ttu-id="926bc-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="926bc-148">RELATED LINKS</span></span>

[<span data-ttu-id="926bc-149">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="926bc-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="926bc-150">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="926bc-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="926bc-151">移除-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="926bc-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


