---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449499"
---
# <span data-ttu-id="a7b3a-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a7b3a-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="a7b3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b3a-103">移除 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7b3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7b3a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7b3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b3a-106">**AzureRmSiteRecoveryFabric** Cmdlet 會移除 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="a7b3a-107">示例</span><span class="sxs-lookup"><span data-stu-id="a7b3a-107">EXAMPLES</span></span>

## <span data-ttu-id="a7b3a-108">參數</span><span class="sxs-lookup"><span data-stu-id="a7b3a-108">PARAMETERS</span></span>

### <span data-ttu-id="a7b3a-109">-結構</span><span class="sxs-lookup"><span data-stu-id="a7b3a-109">-Fabric</span></span>
<span data-ttu-id="a7b3a-110">指定 Azure Site Recovery Fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b3a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a7b3a-111">-Force</span></span>
<span data-ttu-id="a7b3a-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7b3a-113">-確認</span><span class="sxs-lookup"><span data-stu-id="a7b3a-113">-Confirm</span></span>
<span data-ttu-id="a7b3a-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b3a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b3a-115">-WhatIf</span></span>
<span data-ttu-id="a7b3a-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a7b3a-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7b3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b3a-118">-DefaultProfile</span></span>
<span data-ttu-id="a7b3a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7b3a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b3a-120">CommonParameters</span></span>
<span data-ttu-id="a7b3a-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b3a-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7b3a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b3a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a7b3a-123">INPUTS</span></span>

### <span data-ttu-id="a7b3a-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a7b3a-124">ASRFabric</span></span>
<span data-ttu-id="a7b3a-125">形參 "Fabric" 接受來自管線的 "ASRFabric" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a7b3a-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="a7b3a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a7b3a-126">OUTPUTS</span></span>

### <span data-ttu-id="a7b3a-127">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a7b3a-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a7b3a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a7b3a-128">NOTES</span></span>

## <span data-ttu-id="a7b3a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7b3a-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7b3a-130">AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a7b3a-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="a7b3a-131">新-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a7b3a-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
