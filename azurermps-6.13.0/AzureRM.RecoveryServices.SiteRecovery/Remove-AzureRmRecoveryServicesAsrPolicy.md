---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625764"
---
# <span data-ttu-id="f8153-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f8153-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f8153-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8153-102">SYNOPSIS</span></span>
<span data-ttu-id="f8153-103">從 [恢復服務] 保存庫刪除指定的 ASR 複製原則。</span><span class="sxs-lookup"><span data-stu-id="f8153-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8153-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8153-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8153-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8153-105">DESCRIPTION</span></span>
<span data-ttu-id="f8153-106">**AzureRmRecoveryServicesAsrPolicy** Cmdlet 已從復原服務保存庫中刪除指定的複製原則。</span><span class="sxs-lookup"><span data-stu-id="f8153-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="f8153-107">示例</span><span class="sxs-lookup"><span data-stu-id="f8153-107">EXAMPLES</span></span>

### <span data-ttu-id="f8153-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f8153-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="f8153-109">開始刪除指定的複製原則，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f8153-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f8153-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8153-110">PARAMETERS</span></span>

### <span data-ttu-id="f8153-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8153-111">-DefaultProfile</span></span>
<span data-ttu-id="f8153-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8153-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f8153-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8153-113">-InputObject</span></span>
<span data-ttu-id="f8153-114">Cmdlet 的輸入物件：與要刪除之複製原則相對應的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="f8153-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8153-115">-確認</span><span class="sxs-lookup"><span data-stu-id="f8153-115">-Confirm</span></span>
<span data-ttu-id="f8153-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8153-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8153-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8153-117">-WhatIf</span></span>
<span data-ttu-id="f8153-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8153-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8153-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8153-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8153-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8153-120">CommonParameters</span></span>
<span data-ttu-id="f8153-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8153-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8153-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8153-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8153-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f8153-123">INPUTS</span></span>

### <span data-ttu-id="f8153-124">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f8153-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f8153-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f8153-125">OUTPUTS</span></span>

### <span data-ttu-id="f8153-126">System.object</span><span class="sxs-lookup"><span data-stu-id="f8153-126">System.Object</span></span>

## <span data-ttu-id="f8153-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f8153-127">NOTES</span></span>

## <span data-ttu-id="f8153-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8153-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8153-129">AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f8153-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="f8153-130">新-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f8153-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
