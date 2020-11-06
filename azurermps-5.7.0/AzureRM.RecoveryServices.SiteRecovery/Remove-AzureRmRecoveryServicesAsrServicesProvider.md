---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 2aa8855365ea74a00df875fb62bfec49a8c591ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448614"
---
# <span data-ttu-id="23467-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="23467-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="23467-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23467-102">SYNOPSIS</span></span>
<span data-ttu-id="23467-103">從 [恢復服務] 保存庫刪除/取消註冊指定的 Azure Site Recovery 復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="23467-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23467-104">句法</span><span class="sxs-lookup"><span data-stu-id="23467-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23467-105">說明</span><span class="sxs-lookup"><span data-stu-id="23467-105">DESCRIPTION</span></span>
<span data-ttu-id="23467-106">**AzureRmRecoveryServicesAsrServicesProvider** Cmdlet 會從保存庫中移除指定的 Azure Site recovery 復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="23467-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="23467-107">示例</span><span class="sxs-lookup"><span data-stu-id="23467-107">EXAMPLES</span></span>

### <span data-ttu-id="23467-108">範例1</span><span class="sxs-lookup"><span data-stu-id="23467-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="23467-109">啟動指定 Azure 網站復原服務提供者的刪除/登出，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="23467-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="23467-110">參數</span><span class="sxs-lookup"><span data-stu-id="23467-110">PARAMETERS</span></span>

### <span data-ttu-id="23467-111">-確認</span><span class="sxs-lookup"><span data-stu-id="23467-111">-Confirm</span></span>
<span data-ttu-id="23467-112">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="23467-112">Specify if confirmation is required.</span></span> <span data-ttu-id="23467-113">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="23467-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23467-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23467-114">-DefaultProfile</span></span>
<span data-ttu-id="23467-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23467-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23467-116">-Force</span><span class="sxs-lookup"><span data-stu-id="23467-116">-Force</span></span>
<span data-ttu-id="23467-117">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="23467-117">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23467-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23467-118">-InputObject</span></span>
<span data-ttu-id="23467-119">Cmdlet 的輸入物件：對應至要刪除之 ASR 恢復服務提供者的 ASR 恢復服務提供者物件。</span><span class="sxs-lookup"><span data-stu-id="23467-119">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23467-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23467-120">-WhatIf</span></span>
<span data-ttu-id="23467-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23467-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23467-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23467-122">CommonParameters</span></span>
<span data-ttu-id="23467-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23467-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23467-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23467-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23467-125">輸入</span><span class="sxs-lookup"><span data-stu-id="23467-125">INPUTS</span></span>

### <span data-ttu-id="23467-126">RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="23467-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="23467-127">輸出</span><span class="sxs-lookup"><span data-stu-id="23467-127">OUTPUTS</span></span>

### <span data-ttu-id="23467-128">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="23467-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="23467-129">筆記</span><span class="sxs-lookup"><span data-stu-id="23467-129">NOTES</span></span>

## <span data-ttu-id="23467-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="23467-130">RELATED LINKS</span></span>

[<span data-ttu-id="23467-131">AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="23467-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="23467-132">更新-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="23467-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
