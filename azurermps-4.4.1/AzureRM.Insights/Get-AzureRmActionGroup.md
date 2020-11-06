---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 4edb403452d262705fe8fa61691ac77ba4524977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456592"
---
# <span data-ttu-id="01e3f-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="01e3f-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="01e3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="01e3f-103">取得動作群組 (s) 。</span><span class="sxs-lookup"><span data-stu-id="01e3f-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="01e3f-104">SYNTAX</span></span>

### <span data-ttu-id="01e3f-105">BySubscriptionOrResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="01e3f-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01e3f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="01e3f-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01e3f-107">說明</span><span class="sxs-lookup"><span data-stu-id="01e3f-107">DESCRIPTION</span></span>
<span data-ttu-id="01e3f-108">**AzureRmActionGroup** Cmdlet 會取得一或多個動作群組。</span><span class="sxs-lookup"><span data-stu-id="01e3f-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="01e3f-109">示例</span><span class="sxs-lookup"><span data-stu-id="01e3f-109">EXAMPLES</span></span>

### <span data-ttu-id="01e3f-110">範例1：依訂閱識別碼取得動作群組</span><span class="sxs-lookup"><span data-stu-id="01e3f-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="01e3f-111">這個命令會列出目前訂閱的所有動作群組。</span><span class="sxs-lookup"><span data-stu-id="01e3f-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="01e3f-112">範例2：取得指定資源群組的動作群組</span><span class="sxs-lookup"><span data-stu-id="01e3f-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="01e3f-113">這個命令會列出指定資源群組的 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="01e3f-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="01e3f-114">範例3：取得動作群組。</span><span class="sxs-lookup"><span data-stu-id="01e3f-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="01e3f-115">這個命令會列出一個 (清單，其中只有一個元素) [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="01e3f-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="01e3f-116">參數</span><span class="sxs-lookup"><span data-stu-id="01e3f-116">PARAMETERS</span></span>

### <span data-ttu-id="01e3f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="01e3f-117">-Name</span></span>
<span data-ttu-id="01e3f-118">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="01e3f-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e3f-119">-DefaultProfile</span></span>
<span data-ttu-id="01e3f-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01e3f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01e3f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e3f-121">-ResourceGroupName</span></span>
<span data-ttu-id="01e3f-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="01e3f-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e3f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e3f-123">CommonParameters</span></span>
<span data-ttu-id="01e3f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01e3f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e3f-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01e3f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e3f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="01e3f-126">INPUTS</span></span>

### <span data-ttu-id="01e3f-127">所有</span><span class="sxs-lookup"><span data-stu-id="01e3f-127">None</span></span>

## <span data-ttu-id="01e3f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="01e3f-128">OUTPUTS</span></span>

### <span data-ttu-id="01e3f-129"><System.object. 清單 ' 1 [PSActionGroupResource]。 OutputClasses.]</span><span class="sxs-lookup"><span data-stu-id="01e3f-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="01e3f-130">所有</span><span class="sxs-lookup"><span data-stu-id="01e3f-130">None</span></span>

## <span data-ttu-id="01e3f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="01e3f-131">NOTES</span></span>

## <span data-ttu-id="01e3f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="01e3f-132">RELATED LINKS</span></span>

<span data-ttu-id="01e3f-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
[移除-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
[新-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="01e3f-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
