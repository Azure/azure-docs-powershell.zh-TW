---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 82243fbb0ff00c0be46863dba26d8c9a99719598
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398779"
---
# <span data-ttu-id="e6533-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e6533-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="e6533-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6533-102">SYNOPSIS</span></span>
<span data-ttu-id="e6533-103">將動作群組 () 。</span><span class="sxs-lookup"><span data-stu-id="e6533-103">Gets action group(s).</span></span>

## <span data-ttu-id="e6533-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6533-104">SYNTAX</span></span>

### <span data-ttu-id="e6533-105">BySubscriptionOrResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="e6533-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6533-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e6533-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6533-107">描述</span><span class="sxs-lookup"><span data-stu-id="e6533-107">DESCRIPTION</span></span>
<span data-ttu-id="e6533-108">**Get-AzActionGroup** Cmdlet 會取得一或多個動作群組。</span><span class="sxs-lookup"><span data-stu-id="e6533-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="e6533-109">例子</span><span class="sxs-lookup"><span data-stu-id="e6533-109">EXAMPLES</span></span>

### <span data-ttu-id="e6533-110">範例 1：根據訂閱識別碼取得動作群組</span><span class="sxs-lookup"><span data-stu-id="e6533-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="e6533-111">此命令會列出目前訂閱的所有動作群組。</span><span class="sxs-lookup"><span data-stu-id="e6533-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="e6533-112">範例 2：取得給定資源群組的動作群組</span><span class="sxs-lookup"><span data-stu-id="e6533-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="e6533-113">此命令會列出給定資源群組的動作群組。</span><span class="sxs-lookup"><span data-stu-id="e6533-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="e6533-114">範例 3：取得動作群組。</span><span class="sxs-lookup"><span data-stu-id="e6533-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="e6533-115">此命令會列出一 (動作群組中具有單一) 清單。</span><span class="sxs-lookup"><span data-stu-id="e6533-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="e6533-116">參數</span><span class="sxs-lookup"><span data-stu-id="e6533-116">PARAMETERS</span></span>

### <span data-ttu-id="e6533-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6533-117">-DefaultProfile</span></span>
<span data-ttu-id="e6533-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e6533-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6533-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6533-119">-Name</span></span>
<span data-ttu-id="e6533-120">動作組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6533-120">The name of the action group.</span></span>

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

### <span data-ttu-id="e6533-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6533-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6533-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="e6533-122">The resource group name</span></span>

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

### <span data-ttu-id="e6533-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6533-123">CommonParameters</span></span>
<span data-ttu-id="e6533-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6533-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6533-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6533-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6533-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e6533-126">INPUTS</span></span>

### <span data-ttu-id="e6533-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e6533-127">System.String</span></span>

## <span data-ttu-id="e6533-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e6533-128">OUTPUTS</span></span>

### <span data-ttu-id="e6533-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="e6533-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="e6533-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e6533-130">NOTES</span></span>

## <span data-ttu-id="e6533-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6533-131">RELATED LINKS</span></span>

<span data-ttu-id="e6533-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[Remove-AzActionGroup](./Remove-AzActionGroup.md) 
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="e6533-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
