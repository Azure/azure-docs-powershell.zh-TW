---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967312"
---
# <span data-ttu-id="f71f5-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f71f5-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="f71f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f71f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f71f5-103">從 Azure RemoteApp 集合中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="f71f5-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f71f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f71f5-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f71f5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f71f5-105">DESCRIPTION</span></span>
<span data-ttu-id="f71f5-106">**AzureRemoteAppUser** Cmdlet 會從 Azure RemoteApp 集合中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="f71f5-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f71f5-107">示例</span><span class="sxs-lookup"><span data-stu-id="f71f5-107">EXAMPLES</span></span>

### <span data-ttu-id="f71f5-108">Example1：從集合中移除使用者</span><span class="sxs-lookup"><span data-stu-id="f71f5-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="f71f5-109">這個命令會 PattiFuller@contoso.com 從 Contoso 集合中移除 Azure ActiveDirectory 使用者。</span><span class="sxs-lookup"><span data-stu-id="f71f5-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="f71f5-110">參數</span><span class="sxs-lookup"><span data-stu-id="f71f5-110">PARAMETERS</span></span>

### <span data-ttu-id="f71f5-111">-別名</span><span class="sxs-lookup"><span data-stu-id="f71f5-111">-Alias</span></span>
<span data-ttu-id="f71f5-112">指定已發佈的程式別名。</span><span class="sxs-lookup"><span data-stu-id="f71f5-112">Specifies a published program alias.</span></span>
<span data-ttu-id="f71f5-113">您只能在針對每個應用程式發佈模式中使用此參數。</span><span class="sxs-lookup"><span data-stu-id="f71f5-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="f71f5-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f71f5-114">-CollectionName</span></span>
<span data-ttu-id="f71f5-115">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="f71f5-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="f71f5-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f71f5-116">-Profile</span></span>
<span data-ttu-id="f71f5-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f71f5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f71f5-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f71f5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f71f5-119">-類型</span><span class="sxs-lookup"><span data-stu-id="f71f5-119">-Type</span></span>
<span data-ttu-id="f71f5-120">指定使用者類型。</span><span class="sxs-lookup"><span data-stu-id="f71f5-120">Specifies a user type.</span></span>
<span data-ttu-id="f71f5-121">此參數可接受的值為： OrgId 或 MicrosoftAccount。</span><span class="sxs-lookup"><span data-stu-id="f71f5-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="f71f5-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="f71f5-122">-UserUpn</span></span>
<span data-ttu-id="f71f5-123">指定使用者的使用者主要名稱 (UPN) ，例如 user@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="f71f5-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

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

### <span data-ttu-id="f71f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71f5-124">CommonParameters</span></span>
<span data-ttu-id="f71f5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f71f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71f5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f71f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71f5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f71f5-127">INPUTS</span></span>

## <span data-ttu-id="f71f5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f71f5-128">OUTPUTS</span></span>

## <span data-ttu-id="f71f5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f71f5-129">NOTES</span></span>

## <span data-ttu-id="f71f5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f71f5-130">RELATED LINKS</span></span>

[<span data-ttu-id="f71f5-131">附加 AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f71f5-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="f71f5-132">AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f71f5-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


