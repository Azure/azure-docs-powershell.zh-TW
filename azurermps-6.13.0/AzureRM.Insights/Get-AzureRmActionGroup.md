---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 002847ae580e3e3c5d5b44e05ebc1633e4e1574b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624169"
---
# <span data-ttu-id="3a15a-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a15a-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="3a15a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a15a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a15a-103">取得動作群組 (s) 。</span><span class="sxs-lookup"><span data-stu-id="3a15a-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a15a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a15a-104">SYNTAX</span></span>

### <span data-ttu-id="3a15a-105">BySubscriptionOrResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="3a15a-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a15a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3a15a-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a15a-107">說明</span><span class="sxs-lookup"><span data-stu-id="3a15a-107">DESCRIPTION</span></span>
<span data-ttu-id="3a15a-108">**AzureRmActionGroup** Cmdlet 會取得一或多個動作群組。</span><span class="sxs-lookup"><span data-stu-id="3a15a-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="3a15a-109">示例</span><span class="sxs-lookup"><span data-stu-id="3a15a-109">EXAMPLES</span></span>

### <span data-ttu-id="3a15a-110">範例1：依訂閱識別碼取得動作群組</span><span class="sxs-lookup"><span data-stu-id="3a15a-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="3a15a-111">這個命令會列出目前訂閱的所有動作群組。</span><span class="sxs-lookup"><span data-stu-id="3a15a-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="3a15a-112">範例2：取得指定資源群組的動作群組</span><span class="sxs-lookup"><span data-stu-id="3a15a-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="3a15a-113">這個命令會列出指定資源群組的 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="3a15a-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="3a15a-114">範例3：取得動作群組。</span><span class="sxs-lookup"><span data-stu-id="3a15a-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="3a15a-115">這個命令會列出一個 (清單，其中只有一個元素) [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="3a15a-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="3a15a-116">參數</span><span class="sxs-lookup"><span data-stu-id="3a15a-116">PARAMETERS</span></span>

### <span data-ttu-id="3a15a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a15a-117">-DefaultProfile</span></span>
<span data-ttu-id="3a15a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3a15a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a15a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a15a-119">-Name</span></span>
<span data-ttu-id="3a15a-120">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a15a-120">The name of the action group.</span></span>

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

### <span data-ttu-id="3a15a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a15a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a15a-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3a15a-122">The resource group name</span></span>

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

### <span data-ttu-id="3a15a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a15a-123">CommonParameters</span></span>
<span data-ttu-id="3a15a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a15a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a15a-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a15a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a15a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3a15a-126">INPUTS</span></span>

### <span data-ttu-id="3a15a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="3a15a-127">System.String</span></span>

## <span data-ttu-id="3a15a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3a15a-128">OUTPUTS</span></span>

### <span data-ttu-id="3a15a-129">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="3a15a-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="3a15a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3a15a-130">NOTES</span></span>

## <span data-ttu-id="3a15a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a15a-131">RELATED LINKS</span></span>

<span data-ttu-id="3a15a-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
[移除-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
[新-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="3a15a-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
