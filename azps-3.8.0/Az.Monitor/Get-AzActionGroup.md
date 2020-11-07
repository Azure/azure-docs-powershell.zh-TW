---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: c297198a1e49b93d498c136d1cb099d2068d24db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966452"
---
# <span data-ttu-id="270df-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="270df-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="270df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="270df-102">SYNOPSIS</span></span>
<span data-ttu-id="270df-103">取得動作群組 (s) 。</span><span class="sxs-lookup"><span data-stu-id="270df-103">Gets action group(s).</span></span>

## <span data-ttu-id="270df-104">句法</span><span class="sxs-lookup"><span data-stu-id="270df-104">SYNTAX</span></span>

### <span data-ttu-id="270df-105">BySubscriptionOrResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="270df-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="270df-106">ByName</span><span class="sxs-lookup"><span data-stu-id="270df-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="270df-107">說明</span><span class="sxs-lookup"><span data-stu-id="270df-107">DESCRIPTION</span></span>
<span data-ttu-id="270df-108">**AzActionGroup** Cmdlet 會取得一或多個動作群組。</span><span class="sxs-lookup"><span data-stu-id="270df-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="270df-109">示例</span><span class="sxs-lookup"><span data-stu-id="270df-109">EXAMPLES</span></span>

### <span data-ttu-id="270df-110">範例1：依訂閱識別碼取得動作群組</span><span class="sxs-lookup"><span data-stu-id="270df-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="270df-111">這個命令會列出目前訂閱的所有動作群組。</span><span class="sxs-lookup"><span data-stu-id="270df-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="270df-112">範例2：取得指定資源群組的動作群組</span><span class="sxs-lookup"><span data-stu-id="270df-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="270df-113">這個命令會列出指定資源群組的 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="270df-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="270df-114">範例3：取得動作群組。</span><span class="sxs-lookup"><span data-stu-id="270df-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="270df-115">這個命令會列出一個 (清單，其中只有一個元素) [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="270df-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="270df-116">參數</span><span class="sxs-lookup"><span data-stu-id="270df-116">PARAMETERS</span></span>

### <span data-ttu-id="270df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270df-117">-DefaultProfile</span></span>
<span data-ttu-id="270df-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="270df-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="270df-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="270df-119">-Name</span></span>
<span data-ttu-id="270df-120">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="270df-120">The name of the action group.</span></span>

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

### <span data-ttu-id="270df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270df-121">-ResourceGroupName</span></span>
<span data-ttu-id="270df-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="270df-122">The resource group name</span></span>

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

### <span data-ttu-id="270df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270df-123">CommonParameters</span></span>
<span data-ttu-id="270df-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="270df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270df-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="270df-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270df-126">輸入</span><span class="sxs-lookup"><span data-stu-id="270df-126">INPUTS</span></span>

### <span data-ttu-id="270df-127">System.object</span><span class="sxs-lookup"><span data-stu-id="270df-127">System.String</span></span>

## <span data-ttu-id="270df-128">輸出</span><span class="sxs-lookup"><span data-stu-id="270df-128">OUTPUTS</span></span>

### <span data-ttu-id="270df-129">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="270df-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="270df-130">筆記</span><span class="sxs-lookup"><span data-stu-id="270df-130">NOTES</span></span>

## <span data-ttu-id="270df-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="270df-131">RELATED LINKS</span></span>

<span data-ttu-id="270df-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[移除-AzActionGroup](./Remove-AzActionGroup.md) 
[新-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="270df-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
