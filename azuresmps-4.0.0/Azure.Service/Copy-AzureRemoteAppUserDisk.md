---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967144"
---
# <span data-ttu-id="bf313-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="bf313-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="bf313-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf313-102">SYNOPSIS</span></span>
<span data-ttu-id="bf313-103">將使用者的使用者磁片從一個 Azure RemoteApp 集合複製到另一個。</span><span class="sxs-lookup"><span data-stu-id="bf313-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="bf313-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf313-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf313-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf313-105">DESCRIPTION</span></span>
<span data-ttu-id="bf313-106">**Copy AzureRemoteAppUserDisk** Cmdlet 會將使用者的使用者磁片從一個 Azure RemoteApp 集合複製到另一個。</span><span class="sxs-lookup"><span data-stu-id="bf313-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="bf313-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf313-107">EXAMPLES</span></span>

### <span data-ttu-id="bf313-108">範例1：複製使用者磁片</span><span class="sxs-lookup"><span data-stu-id="bf313-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="bf313-109">這個命令會將具有 UPN 的 Azure Active Directory 使用者的使用者磁片 PattiFuller@contoso.com 從集合 Contoso01 複製到 [集合 Contoso02]。</span><span class="sxs-lookup"><span data-stu-id="bf313-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="bf313-110">如果 PattiFuller@contoso.com Contoso02 已存在使用者磁片，這個命令會覆寫。</span><span class="sxs-lookup"><span data-stu-id="bf313-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="bf313-111">參數</span><span class="sxs-lookup"><span data-stu-id="bf313-111">PARAMETERS</span></span>

### <span data-ttu-id="bf313-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="bf313-112">-DestinationCollectionName</span></span>
<span data-ttu-id="bf313-113">指定目的地 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf313-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf313-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="bf313-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="bf313-115">表示此 Cmdlet 會覆寫現有的使用者磁片。</span><span class="sxs-lookup"><span data-stu-id="bf313-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf313-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bf313-116">-Profile</span></span>
<span data-ttu-id="bf313-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bf313-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf313-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bf313-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf313-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="bf313-119">-SourceCollectionName</span></span>
<span data-ttu-id="bf313-120">指定來源 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf313-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf313-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="bf313-121">-UserUpn</span></span>
<span data-ttu-id="bf313-122">指定此 Cmdlet 複製磁片的使用者的使用者主要名稱 (UPN) 。</span><span class="sxs-lookup"><span data-stu-id="bf313-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf313-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf313-123">CommonParameters</span></span>
<span data-ttu-id="bf313-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf313-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf313-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf313-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf313-126">輸入</span><span class="sxs-lookup"><span data-stu-id="bf313-126">INPUTS</span></span>

## <span data-ttu-id="bf313-127">輸出</span><span class="sxs-lookup"><span data-stu-id="bf313-127">OUTPUTS</span></span>

## <span data-ttu-id="bf313-128">筆記</span><span class="sxs-lookup"><span data-stu-id="bf313-128">NOTES</span></span>

## <span data-ttu-id="bf313-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf313-129">RELATED LINKS</span></span>

[<span data-ttu-id="bf313-130">移除-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="bf313-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


