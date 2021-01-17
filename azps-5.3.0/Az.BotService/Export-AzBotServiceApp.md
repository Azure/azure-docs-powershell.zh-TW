---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449964"
---
# <span data-ttu-id="bc8ce-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="bc8ce-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="bc8ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8ce-103">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="bc8ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc8ce-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bc8ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc8ce-105">DESCRIPTION</span></span>
<span data-ttu-id="bc8ce-106">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="bc8ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc8ce-107">EXAMPLES</span></span>

### <span data-ttu-id="bc8ce-108">範例1：下載 BotService 應用程式資料夾</span><span class="sxs-lookup"><span data-stu-id="bc8ce-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="bc8ce-109">下載 BotService App 資料夾</span><span class="sxs-lookup"><span data-stu-id="bc8ce-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="bc8ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc8ce-110">PARAMETERS</span></span>

### <span data-ttu-id="bc8ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8ce-111">-DefaultProfile</span></span>
<span data-ttu-id="bc8ce-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8ce-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc8ce-113">-Name</span></span>
<span data-ttu-id="bc8ce-114">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc8ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc8ce-116">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-116">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8ce-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="bc8ce-117">-SavePath</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8ce-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc8ce-118">-SubscriptionId</span></span>
<span data-ttu-id="bc8ce-119">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-119">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8ce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8ce-120">CommonParameters</span></span>
<span data-ttu-id="bc8ce-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8ce-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8ce-123">輸入</span><span class="sxs-lookup"><span data-stu-id="bc8ce-123">INPUTS</span></span>

## <span data-ttu-id="bc8ce-124">輸出</span><span class="sxs-lookup"><span data-stu-id="bc8ce-124">OUTPUTS</span></span>

### <span data-ttu-id="bc8ce-125">IBot （BotService）。 Api20180712。</span><span class="sxs-lookup"><span data-stu-id="bc8ce-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="bc8ce-126">筆記</span><span class="sxs-lookup"><span data-stu-id="bc8ce-126">NOTES</span></span>

<span data-ttu-id="bc8ce-127">別名</span><span class="sxs-lookup"><span data-stu-id="bc8ce-127">ALIASES</span></span>

## <span data-ttu-id="bc8ce-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc8ce-128">RELATED LINKS</span></span>

