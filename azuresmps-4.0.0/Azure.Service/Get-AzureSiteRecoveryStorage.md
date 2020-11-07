---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967022"
---
# <span data-ttu-id="df94d-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="df94d-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="df94d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df94d-102">SYNOPSIS</span></span>
<span data-ttu-id="df94d-103">取得保存庫的網站復原存儲。</span><span class="sxs-lookup"><span data-stu-id="df94d-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="df94d-104">句法</span><span class="sxs-lookup"><span data-stu-id="df94d-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df94d-105">說明</span><span class="sxs-lookup"><span data-stu-id="df94d-105">DESCRIPTION</span></span>
<span data-ttu-id="df94d-106">**AzureSiteRecoveryStorage** Cmdlet 會針對目前的 Azure site recovery 保存庫取得 Azure Site recovery 存儲。</span><span class="sxs-lookup"><span data-stu-id="df94d-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="df94d-107">示例</span><span class="sxs-lookup"><span data-stu-id="df94d-107">EXAMPLES</span></span>

### <span data-ttu-id="df94d-108">範例1：取得網站恢復儲存空間</span><span class="sxs-lookup"><span data-stu-id="df94d-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="df94d-109">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="df94d-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="df94d-110">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="df94d-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="df94d-111">第二個命令會針對 $Servers 陣列中的第一個伺服器，取得網站復原儲存空間。</span><span class="sxs-lookup"><span data-stu-id="df94d-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="df94d-112">參數</span><span class="sxs-lookup"><span data-stu-id="df94d-112">PARAMETERS</span></span>

### <span data-ttu-id="df94d-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="df94d-113">-Profile</span></span>
<span data-ttu-id="df94d-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="df94d-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="df94d-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="df94d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df94d-116">-伺服器</span><span class="sxs-lookup"><span data-stu-id="df94d-116">-Server</span></span>
<span data-ttu-id="df94d-117">指定 Azure Site Recovery 儲存空間的伺服器。</span><span class="sxs-lookup"><span data-stu-id="df94d-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="df94d-118">若要取得 **ASRServer** 物件，請使用 **AzureSiteRecoveryServer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df94d-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df94d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df94d-119">CommonParameters</span></span>
<span data-ttu-id="df94d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df94d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df94d-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df94d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df94d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="df94d-122">INPUTS</span></span>

## <span data-ttu-id="df94d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="df94d-123">OUTPUTS</span></span>

## <span data-ttu-id="df94d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="df94d-124">NOTES</span></span>

## <span data-ttu-id="df94d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="df94d-125">RELATED LINKS</span></span>

[<span data-ttu-id="df94d-126">AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="df94d-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


