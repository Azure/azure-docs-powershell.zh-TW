---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411580"
---
# <span data-ttu-id="4e880-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="4e880-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="4e880-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e880-102">SYNOPSIS</span></span>
<span data-ttu-id="4e880-103">針對目前的儲存庫，獲得網站修復所管理之網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="4e880-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="4e880-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e880-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e880-105">描述</span><span class="sxs-lookup"><span data-stu-id="4e880-105">DESCRIPTION</span></span>
<span data-ttu-id="4e880-106">**Get-AzureSiteRecoveryNetwork** Cmdlet 會取得目前網站復原庫的 Azure 網站修復網路相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4e880-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="4e880-107">例子</span><span class="sxs-lookup"><span data-stu-id="4e880-107">EXAMPLES</span></span>

### <span data-ttu-id="4e880-108">範例 1：取得網站復原網路</span><span class="sxs-lookup"><span data-stu-id="4e880-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="4e880-109">第一個命令 Cmdlet 會使用 **Get-AzureSiteRecoveryServer** Cmdlet 取得目前 Azure 網站修復保存庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4e880-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="4e880-110">該命令將網站復原伺服器儲存在$Servers變數中。</span><span class="sxs-lookup"><span data-stu-id="4e880-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="4e880-111">第二個命令會為數組中第一個伺服器$Servers網路。</span><span class="sxs-lookup"><span data-stu-id="4e880-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="4e880-112">參數</span><span class="sxs-lookup"><span data-stu-id="4e880-112">PARAMETERS</span></span>

### <span data-ttu-id="4e880-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4e880-113">-Profile</span></span>
<span data-ttu-id="4e880-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e880-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e880-115">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4e880-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e880-116">-Server</span><span class="sxs-lookup"><span data-stu-id="4e880-116">-Server</span></span>
<span data-ttu-id="4e880-117">指定網站復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="4e880-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="4e880-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e880-118">CommonParameters</span></span>
<span data-ttu-id="4e880-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e880-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e880-120">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4e880-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e880-121">輸入</span><span class="sxs-lookup"><span data-stu-id="4e880-121">INPUTS</span></span>

## <span data-ttu-id="4e880-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4e880-122">OUTPUTS</span></span>

## <span data-ttu-id="4e880-123">筆記</span><span class="sxs-lookup"><span data-stu-id="4e880-123">NOTES</span></span>

## <span data-ttu-id="4e880-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e880-124">RELATED LINKS</span></span>




