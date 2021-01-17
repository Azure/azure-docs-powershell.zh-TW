---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286671"
---
# <span data-ttu-id="8f6ed-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8f6ed-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8f6ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6ed-103">更新) 從 Azure Site Recovery 服務提供者收到的資訊， (重新整理伺服器。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="8f6ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f6ed-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f6ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8f6ed-106">**AzRecoveryServicesAsrServicesProvider** Cmdlet 會更新從 Azure Site Recovery 服務提供者收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="8f6ed-107">您可以使用這個 Cmdlet 觸發從復原服務提供者收到的資訊重新整理。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="8f6ed-108">示例</span><span class="sxs-lookup"><span data-stu-id="8f6ed-108">EXAMPLES</span></span>

### <span data-ttu-id="8f6ed-109">範例1</span><span class="sxs-lookup"><span data-stu-id="8f6ed-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="8f6ed-110">開始從指定的 ASR 服務提供者中重新整理資訊的作業，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8f6ed-111">參數</span><span class="sxs-lookup"><span data-stu-id="8f6ed-111">PARAMETERS</span></span>

### <span data-ttu-id="8f6ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6ed-112">-DefaultProfile</span></span>
<span data-ttu-id="8f6ed-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8f6ed-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6ed-114">-InputObject</span></span>
<span data-ttu-id="8f6ed-115">指定 ASR 服務提供者物件，該物件會識別要更新之資訊的伺服器 (進行刷新。 ) </span><span class="sxs-lookup"><span data-stu-id="8f6ed-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ed-116">-確認</span><span class="sxs-lookup"><span data-stu-id="8f6ed-116">-Confirm</span></span>
<span data-ttu-id="8f6ed-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6ed-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6ed-118">-WhatIf</span></span>
<span data-ttu-id="8f6ed-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f6ed-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6ed-121">CommonParameters</span></span>
<span data-ttu-id="8f6ed-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6ed-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8f6ed-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6ed-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8f6ed-124">INPUTS</span></span>

### <span data-ttu-id="8f6ed-125">RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8f6ed-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8f6ed-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8f6ed-126">OUTPUTS</span></span>

### <span data-ttu-id="8f6ed-127">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8f6ed-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8f6ed-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8f6ed-128">NOTES</span></span>

## <span data-ttu-id="8f6ed-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f6ed-129">RELATED LINKS</span></span>

[<span data-ttu-id="8f6ed-130">AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8f6ed-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8f6ed-131">移除-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8f6ed-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
