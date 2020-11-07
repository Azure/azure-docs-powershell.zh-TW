---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626213"
---
# <span data-ttu-id="a2828-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a2828-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="a2828-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2828-102">SYNOPSIS</span></span>
<span data-ttu-id="a2828-103">在網站復原中更新復原方案。</span><span class="sxs-lookup"><span data-stu-id="a2828-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2828-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2828-104">SYNTAX</span></span>

### <span data-ttu-id="a2828-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="a2828-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2828-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="a2828-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2828-107">說明</span><span class="sxs-lookup"><span data-stu-id="a2828-107">DESCRIPTION</span></span>
<span data-ttu-id="a2828-108">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 會在 Azure Site recovery 中更新復原方案，然後發佈該恢復計畫。</span><span class="sxs-lookup"><span data-stu-id="a2828-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="a2828-109">示例</span><span class="sxs-lookup"><span data-stu-id="a2828-109">EXAMPLES</span></span>

### <span data-ttu-id="a2828-110">範例1：更新復原方案</span><span class="sxs-lookup"><span data-stu-id="a2828-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="a2828-111">這個命令會更新指定的復原方案，然後發佈。</span><span class="sxs-lookup"><span data-stu-id="a2828-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="a2828-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2828-112">PARAMETERS</span></span>

### <span data-ttu-id="a2828-113">-Path</span><span class="sxs-lookup"><span data-stu-id="a2828-113">-Path</span></span>
<span data-ttu-id="a2828-114">指定此 Cmdlet 更新之復原方案之恢復計畫檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a2828-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2828-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a2828-115">-RecoveryPlan</span></span>
<span data-ttu-id="a2828-116">指定此 Cmdlet 更新的復原方案。</span><span class="sxs-lookup"><span data-stu-id="a2828-116">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2828-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2828-117">-DefaultProfile</span></span>
<span data-ttu-id="a2828-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2828-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2828-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2828-119">CommonParameters</span></span>
<span data-ttu-id="a2828-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2828-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2828-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2828-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2828-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a2828-122">INPUTS</span></span>

### <span data-ttu-id="a2828-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a2828-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="a2828-124">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a2828-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="a2828-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a2828-125">OUTPUTS</span></span>

## <span data-ttu-id="a2828-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a2828-126">NOTES</span></span>

## <span data-ttu-id="a2828-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2828-127">RELATED LINKS</span></span>

[<span data-ttu-id="a2828-128">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a2828-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a2828-129">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a2828-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a2828-130">移除-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a2828-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


