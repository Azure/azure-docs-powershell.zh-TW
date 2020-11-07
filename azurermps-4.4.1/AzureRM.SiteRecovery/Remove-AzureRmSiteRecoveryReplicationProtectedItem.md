---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625661"
---
# <span data-ttu-id="9bc12-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bc12-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="9bc12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9bc12-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc12-103">移除 Azure Site Recovery 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9bc12-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bc12-104">句法</span><span class="sxs-lookup"><span data-stu-id="9bc12-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bc12-105">說明</span><span class="sxs-lookup"><span data-stu-id="9bc12-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc12-106">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet 會移除 Azure Site Recovery 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9bc12-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="9bc12-107">這個操作會導致複製停止受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9bc12-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="9bc12-108">示例</span><span class="sxs-lookup"><span data-stu-id="9bc12-108">EXAMPLES</span></span>

## <span data-ttu-id="9bc12-109">參數</span><span class="sxs-lookup"><span data-stu-id="9bc12-109">PARAMETERS</span></span>

### <span data-ttu-id="9bc12-110">-Force</span><span class="sxs-lookup"><span data-stu-id="9bc12-110">-Force</span></span>
<span data-ttu-id="9bc12-111">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9bc12-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc12-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bc12-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9bc12-113">指定複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="9bc12-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc12-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9bc12-114">-WaitForCompletion</span></span>
<span data-ttu-id="9bc12-115">表示 Cmdlet 會等待操作完成。</span><span class="sxs-lookup"><span data-stu-id="9bc12-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc12-116">-確認</span><span class="sxs-lookup"><span data-stu-id="9bc12-116">-Confirm</span></span>
<span data-ttu-id="9bc12-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9bc12-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc12-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc12-118">-WhatIf</span></span>
<span data-ttu-id="9bc12-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bc12-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9bc12-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bc12-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc12-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc12-121">-DefaultProfile</span></span>
<span data-ttu-id="9bc12-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bc12-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bc12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc12-123">CommonParameters</span></span>
<span data-ttu-id="9bc12-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9bc12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc12-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9bc12-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc12-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9bc12-126">INPUTS</span></span>

### <span data-ttu-id="9bc12-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bc12-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="9bc12-128">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9bc12-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="9bc12-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9bc12-129">OUTPUTS</span></span>

### <span data-ttu-id="9bc12-130">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9bc12-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9bc12-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9bc12-131">NOTES</span></span>

## <span data-ttu-id="9bc12-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bc12-132">RELATED LINKS</span></span>

[<span data-ttu-id="9bc12-133">AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bc12-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="9bc12-134">新-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bc12-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="9bc12-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9bc12-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
