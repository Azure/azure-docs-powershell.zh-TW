---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967762"
---
# <span data-ttu-id="f9beb-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f9beb-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="f9beb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9beb-102">SYNOPSIS</span></span>
<span data-ttu-id="f9beb-103">列出 Azure RemoteApp 集合中的使用者。</span><span class="sxs-lookup"><span data-stu-id="f9beb-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f9beb-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9beb-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f9beb-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9beb-105">DESCRIPTION</span></span>
<span data-ttu-id="f9beb-106">**AzureRemoteAppUser** Cmdlet 會列出 Azure RemoteApp 集合中的使用者。</span><span class="sxs-lookup"><span data-stu-id="f9beb-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f9beb-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9beb-107">EXAMPLES</span></span>

### <span data-ttu-id="f9beb-108">範例1：列出集合的使用者</span><span class="sxs-lookup"><span data-stu-id="f9beb-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="f9beb-109">這個命令會列出擁有名為 Contoso 之 Azure RemoteApp 集合存取權的使用者。</span><span class="sxs-lookup"><span data-stu-id="f9beb-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="f9beb-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9beb-110">PARAMETERS</span></span>

### <span data-ttu-id="f9beb-111">-別名</span><span class="sxs-lookup"><span data-stu-id="f9beb-111">-Alias</span></span>
<span data-ttu-id="f9beb-112">指定已發佈的程式別名。</span><span class="sxs-lookup"><span data-stu-id="f9beb-112">Specifies a published program alias.</span></span>
<span data-ttu-id="f9beb-113">您只能在針對每個應用程式發佈模式中使用此參數。</span><span class="sxs-lookup"><span data-stu-id="f9beb-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="f9beb-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f9beb-114">-CollectionName</span></span>
<span data-ttu-id="f9beb-115">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9beb-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="f9beb-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f9beb-116">-Profile</span></span>
<span data-ttu-id="f9beb-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9beb-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9beb-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f9beb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9beb-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="f9beb-119">-UserUpn</span></span>
<span data-ttu-id="f9beb-120">指定要列出資訊之使用者的使用者主要名稱 (UPN) 。</span><span class="sxs-lookup"><span data-stu-id="f9beb-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="f9beb-121">例如， PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="f9beb-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f9beb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9beb-122">CommonParameters</span></span>
<span data-ttu-id="f9beb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9beb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9beb-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9beb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9beb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f9beb-125">INPUTS</span></span>

## <span data-ttu-id="f9beb-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f9beb-126">OUTPUTS</span></span>

## <span data-ttu-id="f9beb-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f9beb-127">NOTES</span></span>

## <span data-ttu-id="f9beb-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9beb-128">RELATED LINKS</span></span>

[<span data-ttu-id="f9beb-129">附加 AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f9beb-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="f9beb-130">AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="f9beb-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="f9beb-131">移除-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f9beb-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


