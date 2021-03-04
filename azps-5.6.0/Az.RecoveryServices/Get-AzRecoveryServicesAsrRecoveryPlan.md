---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: d3470c3984026232fc90d336e22668868311aa9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904877"
---
# <span data-ttu-id="ae6dc-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae6dc-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="ae6dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6dc-103">在修復服務庫內獲得復原計畫或所有復原計畫</span><span class="sxs-lookup"><span data-stu-id="ae6dc-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="ae6dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae6dc-104">SYNTAX</span></span>

### <span data-ttu-id="ae6dc-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ae6dc-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae6dc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ae6dc-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae6dc-107">By有LylyName</span><span class="sxs-lookup"><span data-stu-id="ae6dc-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6dc-108">描述</span><span class="sxs-lookup"><span data-stu-id="ae6dc-108">DESCRIPTION</span></span>
<span data-ttu-id="ae6dc-109">**Get-AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會取得指定復原計畫或修復服務庫中所有復原計畫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="ae6dc-110">例子</span><span class="sxs-lookup"><span data-stu-id="ae6dc-110">EXAMPLES</span></span>

### <span data-ttu-id="ae6dc-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ae6dc-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="ae6dc-112">使用指定的名稱來獲得復原計畫。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="ae6dc-113">參數</span><span class="sxs-lookup"><span data-stu-id="ae6dc-113">PARAMETERS</span></span>

### <span data-ttu-id="ae6dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6dc-114">-DefaultProfile</span></span>
<span data-ttu-id="ae6dc-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ae6dc-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ae6dc-116">-FriendlyName</span></span>
<span data-ttu-id="ae6dc-117">指定要取得復原計畫的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="ae6dc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae6dc-118">-Name</span></span>
<span data-ttu-id="ae6dc-119">指定要取得復原計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="ae6dc-120">-路徑</span><span class="sxs-lookup"><span data-stu-id="ae6dc-120">-Path</span></span>
<span data-ttu-id="ae6dc-121">指定此 Cmdlet 會保存復原計畫 json 定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="ae6dc-122">您可以編輯 json 定義來修改復原計畫，並用來透過 Update-AzRecoveryServicesASRRecoveryPlan Cmdlet 更新復原計畫</span><span class="sxs-lookup"><span data-stu-id="ae6dc-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="ae6dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6dc-123">CommonParameters</span></span>
<span data-ttu-id="ae6dc-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae6dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6dc-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae6dc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6dc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ae6dc-126">INPUTS</span></span>

### <span data-ttu-id="ae6dc-127">沒有</span><span class="sxs-lookup"><span data-stu-id="ae6dc-127">None</span></span>

## <span data-ttu-id="ae6dc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ae6dc-128">OUTPUTS</span></span>

### <span data-ttu-id="ae6dc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae6dc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="ae6dc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ae6dc-130">NOTES</span></span>

## <span data-ttu-id="ae6dc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae6dc-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae6dc-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae6dc-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="ae6dc-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae6dc-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="ae6dc-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae6dc-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
