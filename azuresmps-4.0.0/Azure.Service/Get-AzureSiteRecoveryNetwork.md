---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967038"
---
# <span data-ttu-id="9b8ce-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="9b8ce-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="9b8ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8ce-103">取得目前電子倉庫的網站復原所管理網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="9b8ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b8ce-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9b8ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b8ce-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8ce-106">**AzureSiteRecoveryNetwork** Cmdlet 會針對目前的網站復原電子倉庫取得 Azure Site recovery 網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="9b8ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b8ce-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8ce-108">範例1：取得網站恢復網路</span><span class="sxs-lookup"><span data-stu-id="9b8ce-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="9b8ce-109">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="9b8ce-110">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9b8ce-111">第二個命令會針對 $Servers 陣列中的第一個伺服器，取得網站恢復網路。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="9b8ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="9b8ce-112">PARAMETERS</span></span>

### <span data-ttu-id="9b8ce-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9b8ce-113">-Profile</span></span>
<span data-ttu-id="9b8ce-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b8ce-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b8ce-116">-伺服器</span><span class="sxs-lookup"><span data-stu-id="9b8ce-116">-Server</span></span>
<span data-ttu-id="9b8ce-117">指定網站復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="9b8ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8ce-118">CommonParameters</span></span>
<span data-ttu-id="9b8ce-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8ce-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b8ce-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8ce-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9b8ce-121">INPUTS</span></span>

## <span data-ttu-id="9b8ce-122">輸出</span><span class="sxs-lookup"><span data-stu-id="9b8ce-122">OUTPUTS</span></span>

## <span data-ttu-id="9b8ce-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9b8ce-123">NOTES</span></span>

## <span data-ttu-id="9b8ce-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b8ce-124">RELATED LINKS</span></span>

[<span data-ttu-id="9b8ce-125">Azure Site Recovery 服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b8ce-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


