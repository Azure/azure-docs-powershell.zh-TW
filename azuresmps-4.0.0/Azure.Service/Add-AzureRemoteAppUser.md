---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967827"
---
# <span data-ttu-id="9f9b3-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="9f9b3-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="9f9b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f9b3-103">將使用者新增至 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9f9b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f9b3-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9f9b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f9b3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f9b3-106">**載入 AzureRemoteAppUser** Cmdlet 會將使用者新增至 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9f9b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f9b3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f9b3-108">範例1：使用 Microsoft 帳戶新增使用者</span><span class="sxs-lookup"><span data-stu-id="9f9b3-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="9f9b3-109">這個命令會將 Microsoft 帳戶新增 PattiFuller@contoso.com 到名為 Contoso 的集合。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="9f9b3-110">範例2：使用 Azure Active Directory 帳戶新增使用者</span><span class="sxs-lookup"><span data-stu-id="9f9b3-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="9f9b3-111">這個命令會將 Azure Active Directory 帳戶新增 PattiFuller@contoso.com 到名為 Contoso 的集合。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="9f9b3-112">參數</span><span class="sxs-lookup"><span data-stu-id="9f9b3-112">PARAMETERS</span></span>

### <span data-ttu-id="9f9b3-113">-別名</span><span class="sxs-lookup"><span data-stu-id="9f9b3-113">-Alias</span></span>
<span data-ttu-id="9f9b3-114">指定已發佈的程式別名。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-114">Specifies a published program alias.</span></span>
<span data-ttu-id="9f9b3-115">您只能在針對每個應用程式發佈模式中使用此參數。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-115">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f9b3-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9f9b3-116">-CollectionName</span></span>
<span data-ttu-id="9f9b3-117">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f9b3-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9f9b3-118">-Profile</span></span>
<span data-ttu-id="9f9b3-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f9b3-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f9b3-121">-類型</span><span class="sxs-lookup"><span data-stu-id="9f9b3-121">-Type</span></span>
<span data-ttu-id="9f9b3-122">指定使用者類型。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-122">Specifies a user type.</span></span>
<span data-ttu-id="9f9b3-123">此參數可接受的值為： OrgId 或 MicrosoftAccount。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f9b3-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="9f9b3-124">-UserUpn</span></span>
<span data-ttu-id="9f9b3-125">指定使用者的使用者主要名稱 (UPN) ，例如 PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f9b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f9b3-126">CommonParameters</span></span>
<span data-ttu-id="9f9b3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f9b3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f9b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f9b3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9f9b3-129">INPUTS</span></span>

## <span data-ttu-id="9f9b3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9f9b3-130">OUTPUTS</span></span>

## <span data-ttu-id="9f9b3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9f9b3-131">NOTES</span></span>

## <span data-ttu-id="9f9b3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f9b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="9f9b3-133">AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="9f9b3-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="9f9b3-134">移除-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="9f9b3-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


