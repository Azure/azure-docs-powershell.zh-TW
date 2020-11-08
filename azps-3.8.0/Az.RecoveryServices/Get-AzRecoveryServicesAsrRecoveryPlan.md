---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956552"
---
# <span data-ttu-id="809ac-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="809ac-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="809ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="809ac-102">SYNOPSIS</span></span>
<span data-ttu-id="809ac-103">在恢復服務保存庫中取得復原方案或所有復原方案</span><span class="sxs-lookup"><span data-stu-id="809ac-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="809ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="809ac-104">SYNTAX</span></span>

### <span data-ttu-id="809ac-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="809ac-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="809ac-106">ByName</span><span class="sxs-lookup"><span data-stu-id="809ac-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="809ac-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="809ac-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="809ac-108">說明</span><span class="sxs-lookup"><span data-stu-id="809ac-108">DESCRIPTION</span></span>
<span data-ttu-id="809ac-109">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會在復原服務電子倉庫中取得指定的修復方案或所有復原方案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="809ac-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="809ac-110">示例</span><span class="sxs-lookup"><span data-stu-id="809ac-110">EXAMPLES</span></span>

### <span data-ttu-id="809ac-111">範例1</span><span class="sxs-lookup"><span data-stu-id="809ac-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="809ac-112">取得具有指定名稱的復原方案。</span><span class="sxs-lookup"><span data-stu-id="809ac-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="809ac-113">參數</span><span class="sxs-lookup"><span data-stu-id="809ac-113">PARAMETERS</span></span>

### <span data-ttu-id="809ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809ac-114">-DefaultProfile</span></span>
<span data-ttu-id="809ac-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="809ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="809ac-116">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="809ac-116">-FriendlyName</span></span>
<span data-ttu-id="809ac-117">指定要取得的復原方案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="809ac-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="809ac-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="809ac-118">-Name</span></span>
<span data-ttu-id="809ac-119">指定要取得的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="809ac-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="809ac-120">-Path</span><span class="sxs-lookup"><span data-stu-id="809ac-120">-Path</span></span>
<span data-ttu-id="809ac-121">指定此 Cmdlet 儲存恢復方案 json 定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="809ac-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="809ac-122">可以編輯 json 定義來修改恢復計畫，並使用 Update-AzRecoveryServicesASRRecoveryPlan Cmdlet 來更新復原方案</span><span class="sxs-lookup"><span data-stu-id="809ac-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="809ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809ac-123">CommonParameters</span></span>
<span data-ttu-id="809ac-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="809ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809ac-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="809ac-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809ac-126">輸入</span><span class="sxs-lookup"><span data-stu-id="809ac-126">INPUTS</span></span>

### <span data-ttu-id="809ac-127">所有</span><span class="sxs-lookup"><span data-stu-id="809ac-127">None</span></span>

## <span data-ttu-id="809ac-128">輸出</span><span class="sxs-lookup"><span data-stu-id="809ac-128">OUTPUTS</span></span>

### <span data-ttu-id="809ac-129">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="809ac-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="809ac-130">筆記</span><span class="sxs-lookup"><span data-stu-id="809ac-130">NOTES</span></span>

## <span data-ttu-id="809ac-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="809ac-131">RELATED LINKS</span></span>

[<span data-ttu-id="809ac-132">新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="809ac-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="809ac-133">移除-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="809ac-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="809ac-134">更新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="809ac-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)