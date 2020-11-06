---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 57f9009ead66eb87685aaf0142c6dbd8b125f307
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621107"
---
# <span data-ttu-id="ea376-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ea376-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="ea376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea376-102">SYNOPSIS</span></span>
<span data-ttu-id="ea376-103">將 (探索) 物理伺服器新增至可保護的專案清單。</span><span class="sxs-lookup"><span data-stu-id="ea376-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="ea376-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea376-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea376-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea376-105">DESCRIPTION</span></span>
<span data-ttu-id="ea376-106">**新的-AzRecoveryServicesAsrProtectableItem** 會將新的可保護專案新增至在 ASR 結構內的 protection 容器中找到的可保護專案清單中， (只適用于 VMware 結構類型) 。</span><span class="sxs-lookup"><span data-stu-id="ea376-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="ea376-107">示例</span><span class="sxs-lookup"><span data-stu-id="ea376-107">EXAMPLES</span></span>

### <span data-ttu-id="ea376-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ea376-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="ea376-109">新增或探索新的 Azure 恢復服務 ProtectableItem。</span><span class="sxs-lookup"><span data-stu-id="ea376-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="ea376-110">參數</span><span class="sxs-lookup"><span data-stu-id="ea376-110">PARAMETERS</span></span>

### <span data-ttu-id="ea376-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea376-111">-DefaultProfile</span></span>
<span data-ttu-id="ea376-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea376-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea376-113">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ea376-113">-FriendlyName</span></span>
<span data-ttu-id="ea376-114">可保護專案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ea376-114">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="ea376-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="ea376-115">-IPAddress</span></span>
<span data-ttu-id="ea376-116">[能保護的專案] 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ea376-116">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="ea376-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="ea376-117">-OSType</span></span>
<span data-ttu-id="ea376-118">作業系統類型 (Windows/Linux) 的 [能保護的專案]。</span><span class="sxs-lookup"><span data-stu-id="ea376-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea376-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ea376-119">-ProtectionContainer</span></span>
<span data-ttu-id="ea376-120">要新增可保護專案的 ASR 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="ea376-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea376-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ea376-121">-Confirm</span></span>
<span data-ttu-id="ea376-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea376-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea376-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea376-123">-WhatIf</span></span>
<span data-ttu-id="ea376-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea376-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea376-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea376-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea376-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea376-126">CommonParameters</span></span>
<span data-ttu-id="ea376-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea376-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea376-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea376-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea376-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ea376-129">INPUTS</span></span>

### <span data-ttu-id="ea376-130">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ea376-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="ea376-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ea376-131">OUTPUTS</span></span>

### <span data-ttu-id="ea376-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea376-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea376-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ea376-133">NOTES</span></span>

## <span data-ttu-id="ea376-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea376-134">RELATED LINKS</span></span>
