---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625972"
---
# <span data-ttu-id="0b972-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="0b972-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="0b972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b972-102">SYNOPSIS</span></span>
<span data-ttu-id="0b972-103">建立 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="0b972-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b972-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b972-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b972-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b972-105">DESCRIPTION</span></span>
<span data-ttu-id="0b972-106">**新的-AzureRmRecoveryServicesAsrFabric** Cmdlet 會建立指定類型的 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="0b972-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="0b972-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b972-107">EXAMPLES</span></span>

### <span data-ttu-id="0b972-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0b972-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="0b972-109">使用傳遞的名稱開始建立結構，並傳回用於追蹤結構建立作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="0b972-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="0b972-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b972-110">PARAMETERS</span></span>

### <span data-ttu-id="0b972-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b972-111">-Name</span></span>
<span data-ttu-id="0b972-112">指定 Azure 網站復原結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b972-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b972-113">-類型</span><span class="sxs-lookup"><span data-stu-id="0b972-113">-Type</span></span>
<span data-ttu-id="0b972-114">指定 Azure Site Recovery 結構類型。</span><span class="sxs-lookup"><span data-stu-id="0b972-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b972-115">-確認</span><span class="sxs-lookup"><span data-stu-id="0b972-115">-Confirm</span></span>
<span data-ttu-id="0b972-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b972-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b972-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b972-117">-WhatIf</span></span>
<span data-ttu-id="0b972-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b972-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b972-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b972-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b972-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b972-120">CommonParameters</span></span>
<span data-ttu-id="0b972-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b972-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b972-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b972-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b972-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0b972-123">INPUTS</span></span>

### <span data-ttu-id="0b972-124">所有</span><span class="sxs-lookup"><span data-stu-id="0b972-124">None</span></span>

## <span data-ttu-id="0b972-125">輸出</span><span class="sxs-lookup"><span data-stu-id="0b972-125">OUTPUTS</span></span>

### <span data-ttu-id="0b972-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b972-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b972-127">筆記</span><span class="sxs-lookup"><span data-stu-id="0b972-127">NOTES</span></span>

## <span data-ttu-id="0b972-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b972-128">RELATED LINKS</span></span>

[<span data-ttu-id="0b972-129">AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="0b972-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="0b972-130">移除-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="0b972-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
