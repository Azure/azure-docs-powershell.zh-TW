---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967555"
---
# <span data-ttu-id="c5d48-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c5d48-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="c5d48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5d48-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d48-103">移除網站恢復電子倉庫的儲存物件對應。</span><span class="sxs-lookup"><span data-stu-id="c5d48-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="c5d48-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5d48-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5d48-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5d48-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d48-106">**AzureSiteRecoveryStorageMapping** Cmdlet 會移除目前 Azure Site Recovery 保存庫的儲存物件對應。</span><span class="sxs-lookup"><span data-stu-id="c5d48-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c5d48-107">示例</span><span class="sxs-lookup"><span data-stu-id="c5d48-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d48-108">範例1：移除網路與恢復網路之間的對應</span><span class="sxs-lookup"><span data-stu-id="c5d48-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="c5d48-109">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="c5d48-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="c5d48-110">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="c5d48-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="c5d48-111">第二個命令會取得兩個儲存物件之間的對應，然後將它儲存在 $StorageMapping 變數中。</span><span class="sxs-lookup"><span data-stu-id="c5d48-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="c5d48-112">命令會將網路對應的主伺服器指定為 $Servers 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="c5d48-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="c5d48-113">該命令會將恢復網路的伺服器指定為 $Servers 的第二個元素。</span><span class="sxs-lookup"><span data-stu-id="c5d48-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="c5d48-114">最後一個命令會移除 $StorageMapping 中的對應。</span><span class="sxs-lookup"><span data-stu-id="c5d48-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="c5d48-115">參數</span><span class="sxs-lookup"><span data-stu-id="c5d48-115">PARAMETERS</span></span>

### <span data-ttu-id="c5d48-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c5d48-116">-Profile</span></span>
<span data-ttu-id="c5d48-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c5d48-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5d48-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c5d48-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5d48-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="c5d48-119">-StorageMapping</span></span>
<span data-ttu-id="c5d48-120">指定網路對應。</span><span class="sxs-lookup"><span data-stu-id="c5d48-120">Specifies a network mapping.</span></span>
<span data-ttu-id="c5d48-121">若要取得 **ASRStorageMapping** ，請使用 **AzureSiteRecoveryStorage** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5d48-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d48-122">CommonParameters</span></span>
<span data-ttu-id="c5d48-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5d48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d48-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5d48-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d48-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c5d48-125">INPUTS</span></span>

## <span data-ttu-id="c5d48-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c5d48-126">OUTPUTS</span></span>

## <span data-ttu-id="c5d48-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c5d48-127">NOTES</span></span>

## <span data-ttu-id="c5d48-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5d48-128">RELATED LINKS</span></span>

[<span data-ttu-id="c5d48-129">AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="c5d48-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


