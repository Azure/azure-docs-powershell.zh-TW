---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967021"
---
# <span data-ttu-id="e165e-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="e165e-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="e165e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e165e-102">SYNOPSIS</span></span>
<span data-ttu-id="e165e-103">取得保存庫的網站復原儲存物件對應。</span><span class="sxs-lookup"><span data-stu-id="e165e-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="e165e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e165e-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e165e-105">說明</span><span class="sxs-lookup"><span data-stu-id="e165e-105">DESCRIPTION</span></span>
<span data-ttu-id="e165e-106">**AzureSiteRecoveryStorageMapping** Cmdlet 會針對目前的 Azure site recovery 保存庫取得 Azure Site Recovery 儲存空間物件的鏡像。</span><span class="sxs-lookup"><span data-stu-id="e165e-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e165e-107">示例</span><span class="sxs-lookup"><span data-stu-id="e165e-107">EXAMPLES</span></span>

### <span data-ttu-id="e165e-108">範例1：取得儲存物件與恢復儲存物件之間的對應</span><span class="sxs-lookup"><span data-stu-id="e165e-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="e165e-109">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="e165e-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="e165e-110">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="e165e-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="e165e-111">第二個命令會取得兩個 Azure 儲存空間物件之間的對應。</span><span class="sxs-lookup"><span data-stu-id="e165e-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="e165e-112">該命令會將儲存物件對應的主要伺服器指定為 $Servers 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="e165e-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="e165e-113">該命令會將恢復儲存物件的伺服器指定為 $Servers 的第二個元素。</span><span class="sxs-lookup"><span data-stu-id="e165e-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="e165e-114">參數</span><span class="sxs-lookup"><span data-stu-id="e165e-114">PARAMETERS</span></span>

### <span data-ttu-id="e165e-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="e165e-115">-PrimaryServer</span></span>
<span data-ttu-id="e165e-116">指定主要伺服器。</span><span class="sxs-lookup"><span data-stu-id="e165e-116">Specifies the primary server.</span></span>
<span data-ttu-id="e165e-117">若要取得伺服器，請使用 **AzureSiteRecoveryServer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e165e-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e165e-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e165e-118">-Profile</span></span>
<span data-ttu-id="e165e-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e165e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e165e-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e165e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e165e-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e165e-121">-RecoveryServer</span></span>
<span data-ttu-id="e165e-122">指定復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="e165e-122">Specifies the recovery server.</span></span>
<span data-ttu-id="e165e-123">若要取得伺服器，請使用 **AzureSiteRecoveryServer** 。</span><span class="sxs-lookup"><span data-stu-id="e165e-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e165e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e165e-124">CommonParameters</span></span>
<span data-ttu-id="e165e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e165e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e165e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e165e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e165e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e165e-127">INPUTS</span></span>

## <span data-ttu-id="e165e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e165e-128">OUTPUTS</span></span>

## <span data-ttu-id="e165e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e165e-129">NOTES</span></span>

## <span data-ttu-id="e165e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e165e-130">RELATED LINKS</span></span>

[<span data-ttu-id="e165e-131">AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e165e-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="e165e-132">新-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="e165e-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="e165e-133">移除-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="e165e-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


