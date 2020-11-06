---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456200"
---
# <span data-ttu-id="fb9f2-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb9f2-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="fb9f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9f2-103">取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb9f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb9f2-104">SYNTAX</span></span>

### <span data-ttu-id="fb9f2-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb9f2-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9f2-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb9f2-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb9f2-107">說明</span><span class="sxs-lookup"><span data-stu-id="fb9f2-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9f2-108">**AzureRmActivityLogAlert** Cmdlet 會取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="fb9f2-109">示例</span><span class="sxs-lookup"><span data-stu-id="fb9f2-109">EXAMPLES</span></span>

### <span data-ttu-id="fb9f2-110">範例1：依訂閱識別碼取得活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="fb9f2-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="fb9f2-111">這個命令會列出目前訂閱的所有活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="fb9f2-112">範例2：取得特定資源群組的活動記錄警報</span><span class="sxs-lookup"><span data-stu-id="fb9f2-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="fb9f2-113">這個命令會列出特定資源群組的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="fb9f2-114">範例3：取得活動記錄警示。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="fb9f2-115">這個命令會列出一個 (清單，其中只有一個元素) 活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="fb9f2-116">參數</span><span class="sxs-lookup"><span data-stu-id="fb9f2-116">PARAMETERS</span></span>

### <span data-ttu-id="fb9f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9f2-117">-DefaultProfile</span></span>
<span data-ttu-id="fb9f2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fb9f2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb9f2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb9f2-119">-Name</span></span>
<span data-ttu-id="fb9f2-120">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-120">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb9f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb9f2-122">警示資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="fb9f2-123">如果 Name 不是 null 或空，此參數必須包含且非空字串。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9f2-124">CommonParameters</span></span>
<span data-ttu-id="fb9f2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9f2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb9f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9f2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fb9f2-127">INPUTS</span></span>

### <span data-ttu-id="fb9f2-128">所有</span><span class="sxs-lookup"><span data-stu-id="fb9f2-128">None</span></span>

## <span data-ttu-id="fb9f2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fb9f2-129">OUTPUTS</span></span>

### <span data-ttu-id="fb9f2-130"><System.object. 清單 ' 1 [PSActivityLogAlertResource]。 OutputClasses.]</span><span class="sxs-lookup"><span data-stu-id="fb9f2-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="fb9f2-131">所有</span><span class="sxs-lookup"><span data-stu-id="fb9f2-131">None</span></span>

## <span data-ttu-id="fb9f2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fb9f2-132">NOTES</span></span>

## <span data-ttu-id="fb9f2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb9f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb9f2-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb9f2-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fb9f2-135">更新-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb9f2-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fb9f2-136">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb9f2-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fb9f2-137">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="fb9f2-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="fb9f2-138">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="fb9f2-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
