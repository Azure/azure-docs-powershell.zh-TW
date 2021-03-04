---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903510"
---
# <span data-ttu-id="fb22a-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="fb22a-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="fb22a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb22a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb22a-103">定義新的 Office 365 流量中斷策略，以用於虛擬裝置網站。</span><span class="sxs-lookup"><span data-stu-id="fb22a-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="fb22a-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb22a-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb22a-105">描述</span><span class="sxs-lookup"><span data-stu-id="fb22a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb22a-106">命令New-AzOffice365PolicyProperties定義要與虛擬裝置網站一起使用的 Office 365 中斷群組原則。</span><span class="sxs-lookup"><span data-stu-id="fb22a-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="fb22a-107">例子</span><span class="sxs-lookup"><span data-stu-id="fb22a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb22a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fb22a-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="fb22a-109">建立 Office 365 流量中斷策略物件，以與虛擬裝置網站命令一起使用。</span><span class="sxs-lookup"><span data-stu-id="fb22a-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="fb22a-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb22a-110">PARAMETERS</span></span>

### <span data-ttu-id="fb22a-111">-允許</span><span class="sxs-lookup"><span data-stu-id="fb22a-111">-Allow</span></span>
<span data-ttu-id="fb22a-112">中斷允許類別流量。</span><span class="sxs-lookup"><span data-stu-id="fb22a-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb22a-113">-預設</span><span class="sxs-lookup"><span data-stu-id="fb22a-113">-Default</span></span>
<span data-ttu-id="fb22a-114">中斷預設類別流量。</span><span class="sxs-lookup"><span data-stu-id="fb22a-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb22a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb22a-115">-DefaultProfile</span></span>
<span data-ttu-id="fb22a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb22a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb22a-117">-優化</span><span class="sxs-lookup"><span data-stu-id="fb22a-117">-Optimize</span></span>
<span data-ttu-id="fb22a-118">分組優化類別流量。</span><span class="sxs-lookup"><span data-stu-id="fb22a-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb22a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb22a-119">CommonParameters</span></span>
<span data-ttu-id="fb22a-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb22a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb22a-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb22a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb22a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fb22a-122">INPUTS</span></span>

### <span data-ttu-id="fb22a-123">沒有</span><span class="sxs-lookup"><span data-stu-id="fb22a-123">None</span></span>

## <span data-ttu-id="fb22a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fb22a-124">OUTPUTS</span></span>

### <span data-ttu-id="fb22a-125">Microsoft.Azure.Commands.Network.models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="fb22a-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="fb22a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fb22a-126">NOTES</span></span>

## <span data-ttu-id="fb22a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb22a-127">RELATED LINKS</span></span>
