---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450931"
---
# <span data-ttu-id="2eea5-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2eea5-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="2eea5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2eea5-102">SYNOPSIS</span></span>
<span data-ttu-id="2eea5-103">註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="2eea5-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eea5-104">句法</span><span class="sxs-lookup"><span data-stu-id="2eea5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eea5-105">說明</span><span class="sxs-lookup"><span data-stu-id="2eea5-105">DESCRIPTION</span></span>
<span data-ttu-id="2eea5-106">**新的-AzureRmApiManagementUser** Cmdlet 會註冊新的使用者。</span><span class="sxs-lookup"><span data-stu-id="2eea5-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="2eea5-107">示例</span><span class="sxs-lookup"><span data-stu-id="2eea5-107">EXAMPLES</span></span>

### <span data-ttu-id="2eea5-108">範例1：註冊新的使用者</span><span class="sxs-lookup"><span data-stu-id="2eea5-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="2eea5-109">這個命令會將一個名為 Patti 的新使用者更完整。</span><span class="sxs-lookup"><span data-stu-id="2eea5-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="2eea5-110">參數</span><span class="sxs-lookup"><span data-stu-id="2eea5-110">PARAMETERS</span></span>

### <span data-ttu-id="2eea5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="2eea5-111">-Context</span></span>
<span data-ttu-id="2eea5-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2eea5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2eea5-113">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="2eea5-113">-Email</span></span>
<span data-ttu-id="2eea5-114">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="2eea5-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="2eea5-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="2eea5-115">-FirstName</span></span>
<span data-ttu-id="2eea5-116">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="2eea5-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="2eea5-117">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="2eea5-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="2eea5-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="2eea5-118">-LastName</span></span>
<span data-ttu-id="2eea5-119">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="2eea5-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="2eea5-120">這個參數必須是1到100個字元長。</span><span class="sxs-lookup"><span data-stu-id="2eea5-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="2eea5-121">-記事</span><span class="sxs-lookup"><span data-stu-id="2eea5-121">-Note</span></span>
<span data-ttu-id="2eea5-122">指定使用者的相關記事。</span><span class="sxs-lookup"><span data-stu-id="2eea5-122">Specifies a note about the user.</span></span>
<span data-ttu-id="2eea5-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2eea5-123">This parameter is optional.</span></span>
<span data-ttu-id="2eea5-124">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2eea5-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="2eea5-125">-Password</span><span class="sxs-lookup"><span data-stu-id="2eea5-125">-Password</span></span>
<span data-ttu-id="2eea5-126">指定使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="2eea5-126">Specifies the user password.</span></span>
<span data-ttu-id="2eea5-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2eea5-127">This parameter is required.</span></span>

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

### <span data-ttu-id="2eea5-128">-State</span><span class="sxs-lookup"><span data-stu-id="2eea5-128">-State</span></span>
<span data-ttu-id="2eea5-129">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="2eea5-129">Specifies the user state.</span></span>
<span data-ttu-id="2eea5-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2eea5-130">This parameter is optional.</span></span>
<span data-ttu-id="2eea5-131">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2eea5-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eea5-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="2eea5-132">-UserId</span></span>
<span data-ttu-id="2eea5-133">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eea5-133">Specifies the user ID.</span></span>
<span data-ttu-id="2eea5-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2eea5-134">This parameter is optional.</span></span>
<span data-ttu-id="2eea5-135">如果未指定此參數，此 Cmdlet 會產生使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eea5-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="2eea5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eea5-136">-DefaultProfile</span></span>
<span data-ttu-id="2eea5-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2eea5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eea5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eea5-138">CommonParameters</span></span>
<span data-ttu-id="2eea5-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2eea5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eea5-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2eea5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eea5-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2eea5-141">INPUTS</span></span>

## <span data-ttu-id="2eea5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="2eea5-142">OUTPUTS</span></span>

### <span data-ttu-id="2eea5-143">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2eea5-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="2eea5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="2eea5-144">NOTES</span></span>

## <span data-ttu-id="2eea5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="2eea5-145">RELATED LINKS</span></span>

[<span data-ttu-id="2eea5-146">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2eea5-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="2eea5-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2eea5-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


