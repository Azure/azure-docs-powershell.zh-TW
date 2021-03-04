---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904141"
---
# <span data-ttu-id="5fb71-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="5fb71-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="5fb71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5fb71-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb71-103">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="5fb71-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="5fb71-104">語法</span><span class="sxs-lookup"><span data-stu-id="5fb71-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5fb71-105">描述</span><span class="sxs-lookup"><span data-stu-id="5fb71-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb71-106">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="5fb71-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="5fb71-107">例子</span><span class="sxs-lookup"><span data-stu-id="5fb71-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb71-108">範例 1：向下載入 BotService App 資料夾</span><span class="sxs-lookup"><span data-stu-id="5fb71-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="5fb71-109">向下載入 BotService 應用程式資料夾</span><span class="sxs-lookup"><span data-stu-id="5fb71-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="5fb71-110">參數</span><span class="sxs-lookup"><span data-stu-id="5fb71-110">PARAMETERS</span></span>

### <span data-ttu-id="5fb71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb71-111">-DefaultProfile</span></span>
<span data-ttu-id="5fb71-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5fb71-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb71-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fb71-113">-Name</span></span>
<span data-ttu-id="5fb71-114">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fb71-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="5fb71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb71-115">-ResourceGroupName</span></span>
<span data-ttu-id="5fb71-116">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="5fb71-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="5fb71-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="5fb71-117">-SavePath</span></span>


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

### <span data-ttu-id="5fb71-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fb71-118">-SubscriptionId</span></span>
<span data-ttu-id="5fb71-119">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5fb71-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5fb71-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb71-120">CommonParameters</span></span>
<span data-ttu-id="5fb71-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5fb71-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb71-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fb71-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb71-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5fb71-123">INPUTS</span></span>

## <span data-ttu-id="5fb71-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5fb71-124">OUTPUTS</span></span>

### <span data-ttu-id="5fb71-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="5fb71-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="5fb71-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5fb71-126">NOTES</span></span>

<span data-ttu-id="5fb71-127">別名</span><span class="sxs-lookup"><span data-stu-id="5fb71-127">ALIASES</span></span>

## <span data-ttu-id="5fb71-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fb71-128">RELATED LINKS</span></span>

