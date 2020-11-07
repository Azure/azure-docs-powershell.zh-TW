---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967421"
---
# <span data-ttu-id="b664e-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b664e-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="b664e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b664e-102">SYNOPSIS</span></span>
<span data-ttu-id="b664e-103">建立 Azure 儲存空間物件與復原儲存物件之間的對應。</span><span class="sxs-lookup"><span data-stu-id="b664e-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="b664e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b664e-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b664e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b664e-105">DESCRIPTION</span></span>
<span data-ttu-id="b664e-106">**新的-AzureSiteRecoveryStorageMapping** Cmdlet 會在 Azure Site Recovery 管理的主要 Azure 儲存空間物件與復原儲存物件之間建立對應。</span><span class="sxs-lookup"><span data-stu-id="b664e-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="b664e-107">示例</span><span class="sxs-lookup"><span data-stu-id="b664e-107">EXAMPLES</span></span>

### <span data-ttu-id="b664e-108">範例1：建立儲存物件與恢復儲存物件之間的對應</span><span class="sxs-lookup"><span data-stu-id="b664e-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="b664e-109">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="b664e-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b664e-110">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="b664e-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b664e-111">第二個命令會針對 $Servers 陣列中的第一個伺服器，取得網站復原儲存空間，然後將其儲存在 $Storages 中。</span><span class="sxs-lookup"><span data-stu-id="b664e-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="b664e-112">最後一個命令會在主要網路和恢復網路之間建立對應。</span><span class="sxs-lookup"><span data-stu-id="b664e-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="b664e-113">該命令會將主要儲存物件指定為 $Storages 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="b664e-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="b664e-114">該命令會將復原儲存物件指定為 $Storages 的第二個元素。</span><span class="sxs-lookup"><span data-stu-id="b664e-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="b664e-115">參數</span><span class="sxs-lookup"><span data-stu-id="b664e-115">PARAMETERS</span></span>

### <span data-ttu-id="b664e-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="b664e-116">-PrimaryStorage</span></span>
<span data-ttu-id="b664e-117">指定要對應至恢復儲存空間的主要儲存空間。</span><span class="sxs-lookup"><span data-stu-id="b664e-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="b664e-118">若要取得 **ASRStorage** 物件，請使用 Get-AzureSiteRecoveryStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b664e-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b664e-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b664e-119">-Profile</span></span>
<span data-ttu-id="b664e-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b664e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b664e-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b664e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b664e-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="b664e-122">-RecoveryStorage</span></span>
<span data-ttu-id="b664e-123">指定復原儲存物件。</span><span class="sxs-lookup"><span data-stu-id="b664e-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="b664e-124">這個 Cmdlet 會將主要儲存物件對應至此參數指定的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="b664e-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="b664e-125">若要取得 **ASRStorage** 物件，請使用 **AzureSiteRecoveryStorage** 。</span><span class="sxs-lookup"><span data-stu-id="b664e-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b664e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b664e-126">CommonParameters</span></span>
<span data-ttu-id="b664e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b664e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b664e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b664e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b664e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b664e-129">INPUTS</span></span>

## <span data-ttu-id="b664e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b664e-130">OUTPUTS</span></span>

## <span data-ttu-id="b664e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b664e-131">NOTES</span></span>

## <span data-ttu-id="b664e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b664e-132">RELATED LINKS</span></span>

[<span data-ttu-id="b664e-133">AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="b664e-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="b664e-134">AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b664e-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="b664e-135">移除-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="b664e-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


