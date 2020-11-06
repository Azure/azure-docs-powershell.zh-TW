---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: c27d4d88dd4c2fdf86db5ca39d608add2feb845f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443727"
---
# <span data-ttu-id="d0283-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="d0283-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="d0283-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0283-102">SYNOPSIS</span></span>
<span data-ttu-id="d0283-103">新增 vCenter 伺服器以探索可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="d0283-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0283-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0283-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0283-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0283-105">DESCRIPTION</span></span>
<span data-ttu-id="d0283-106">**新的-AzureRmRecoveryServicesAsrvCenter** Cmdlet 會新增 vCenter 伺服器來探索可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="d0283-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="d0283-107">這個 Cmdlet 會註冊 vCenter 伺服器以供在佈建服務器中探索。</span><span class="sxs-lookup"><span data-stu-id="d0283-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="d0283-108">示例</span><span class="sxs-lookup"><span data-stu-id="d0283-108">EXAMPLES</span></span>

### <span data-ttu-id="d0283-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d0283-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="d0283-110">新增 vCenter 伺服器以探索可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="d0283-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="d0283-111">參數</span><span class="sxs-lookup"><span data-stu-id="d0283-111">PARAMETERS</span></span>

### <span data-ttu-id="d0283-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d0283-112">-Account</span></span>
<span data-ttu-id="d0283-113">使用者登入 creadential 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d0283-113">User login creadential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0283-114">-DefaultProfile</span></span>
<span data-ttu-id="d0283-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0283-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-116">-結構</span><span class="sxs-lookup"><span data-stu-id="d0283-116">-Fabric</span></span>
<span data-ttu-id="d0283-117">與佈建服務器相對應的 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="d0283-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="d0283-118">-IpOrHostName</span></span>
<span data-ttu-id="d0283-119">VCenter 伺服器的 IPv4 位址或 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d0283-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0283-120">-Name</span></span>
<span data-ttu-id="d0283-121">VCenter 伺服器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="d0283-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-122">-埠</span><span class="sxs-lookup"><span data-stu-id="d0283-122">-Port</span></span>
<span data-ttu-id="d0283-123">VCenter 伺服器上用來進行探索的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="d0283-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d0283-124">-Confirm</span></span>
<span data-ttu-id="d0283-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0283-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0283-126">-WhatIf</span></span>
<span data-ttu-id="d0283-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0283-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0283-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0283-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0283-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0283-129">CommonParameters</span></span>
<span data-ttu-id="d0283-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0283-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0283-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0283-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0283-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d0283-132">INPUTS</span></span>

### <span data-ttu-id="d0283-133">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d0283-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d0283-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d0283-134">OUTPUTS</span></span>

### <span data-ttu-id="d0283-135">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 0.1.1.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="d0283-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d0283-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d0283-136">NOTES</span></span>

## <span data-ttu-id="d0283-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0283-137">RELATED LINKS</span></span>
