---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: a10f7ffb1b05474e5d2b86fa7d7a55f825aaad25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626239"
---
# <span data-ttu-id="71b0a-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b0a-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="71b0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="71b0a-103">在恢復服務保存庫中取得復原方案或所有復原方案</span><span class="sxs-lookup"><span data-stu-id="71b0a-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71b0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="71b0a-104">SYNTAX</span></span>

### <span data-ttu-id="71b0a-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="71b0a-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [<CommonParameters>]
```

### <span data-ttu-id="71b0a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="71b0a-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>] [<CommonParameters>]
```

### <span data-ttu-id="71b0a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="71b0a-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>] [<CommonParameters>]
```

## <span data-ttu-id="71b0a-108">說明</span><span class="sxs-lookup"><span data-stu-id="71b0a-108">DESCRIPTION</span></span>
<span data-ttu-id="71b0a-109">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 會在復原服務電子倉庫中取得指定的修復方案或所有復原方案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="71b0a-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="71b0a-110">示例</span><span class="sxs-lookup"><span data-stu-id="71b0a-110">EXAMPLES</span></span>

### <span data-ttu-id="71b0a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="71b0a-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="71b0a-112">取得具有指定名稱的復原方案。</span><span class="sxs-lookup"><span data-stu-id="71b0a-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="71b0a-113">參數</span><span class="sxs-lookup"><span data-stu-id="71b0a-113">PARAMETERS</span></span>

### <span data-ttu-id="71b0a-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="71b0a-114">-FriendlyName</span></span>
<span data-ttu-id="71b0a-115">指定要取得的復原方案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="71b0a-115">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b0a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="71b0a-116">-Name</span></span>
<span data-ttu-id="71b0a-117">指定要取得的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="71b0a-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b0a-118">-Path</span><span class="sxs-lookup"><span data-stu-id="71b0a-118">-Path</span></span>
<span data-ttu-id="71b0a-119">指定此 Cmdlet 儲存恢復方案 json 定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="71b0a-119">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="71b0a-120">可以編輯 json 定義來修改恢復計畫，並使用 Update-AzureRmRecoveryServicesASRRecoveryPlan Cmdlet 來更新復原方案</span><span class="sxs-lookup"><span data-stu-id="71b0a-120">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b0a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b0a-121">CommonParameters</span></span>
<span data-ttu-id="71b0a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71b0a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b0a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71b0a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b0a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="71b0a-124">INPUTS</span></span>

### <span data-ttu-id="71b0a-125">所有</span><span class="sxs-lookup"><span data-stu-id="71b0a-125">None</span></span>

## <span data-ttu-id="71b0a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="71b0a-126">OUTPUTS</span></span>

### <span data-ttu-id="71b0a-127">System.object. IEnumerable "1 [ASRRecoveryPlan，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="71b0a-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="71b0a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="71b0a-128">NOTES</span></span>

## <span data-ttu-id="71b0a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="71b0a-129">RELATED LINKS</span></span>

[<span data-ttu-id="71b0a-130">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b0a-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="71b0a-131">移除-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b0a-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="71b0a-132">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71b0a-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
