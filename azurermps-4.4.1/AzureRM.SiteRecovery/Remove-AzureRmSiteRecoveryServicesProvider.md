---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447951"
---
# <span data-ttu-id="a164f-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a164f-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="a164f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a164f-102">SYNOPSIS</span></span>
<span data-ttu-id="a164f-103">移除 Azure Site Recovery 服務提供者。</span><span class="sxs-lookup"><span data-stu-id="a164f-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a164f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a164f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a164f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a164f-105">DESCRIPTION</span></span>
<span data-ttu-id="a164f-106">**AzureRmSiteRecoveryServicesProvider** Cmdlet 會從保存庫中移除 Azure Site Recovery 服務提供者。</span><span class="sxs-lookup"><span data-stu-id="a164f-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="a164f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a164f-107">EXAMPLES</span></span>

## <span data-ttu-id="a164f-108">參數</span><span class="sxs-lookup"><span data-stu-id="a164f-108">PARAMETERS</span></span>

### <span data-ttu-id="a164f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="a164f-109">-Force</span></span>
<span data-ttu-id="a164f-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a164f-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a164f-111">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a164f-111">-ServicesProvider</span></span>
<span data-ttu-id="a164f-112">指定服務提供者物件。</span><span class="sxs-lookup"><span data-stu-id="a164f-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a164f-113">-確認</span><span class="sxs-lookup"><span data-stu-id="a164f-113">-Confirm</span></span>
<span data-ttu-id="a164f-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a164f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a164f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a164f-115">-WhatIf</span></span>
<span data-ttu-id="a164f-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a164f-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a164f-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a164f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a164f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a164f-118">-DefaultProfile</span></span>
<span data-ttu-id="a164f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a164f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a164f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a164f-120">CommonParameters</span></span>
<span data-ttu-id="a164f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a164f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a164f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a164f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a164f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a164f-123">INPUTS</span></span>

### <span data-ttu-id="a164f-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a164f-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="a164f-125">形參 "ServicesProvider" 接受管線中 "ASRRecoveryServicesProvider" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a164f-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="a164f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a164f-126">OUTPUTS</span></span>

### <span data-ttu-id="a164f-127">System.object. IEnumerable "1 [ASRJob，SiteRecovery，Version = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （SiteRecovery =，Culture = 中立）</span><span class="sxs-lookup"><span data-stu-id="a164f-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a164f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a164f-128">NOTES</span></span>

## <span data-ttu-id="a164f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a164f-129">RELATED LINKS</span></span>

[<span data-ttu-id="a164f-130">AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a164f-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="a164f-131">更新-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a164f-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
