---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135811"
---
# <span data-ttu-id="b79d7-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="b79d7-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="b79d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b79d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b79d7-103">定義要與虛擬裝置網站搭配使用的新 Office 365 流量排列原則。</span><span class="sxs-lookup"><span data-stu-id="b79d7-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="b79d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b79d7-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b79d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="b79d7-105">DESCRIPTION</span></span>
<span data-ttu-id="b79d7-106">[New-AzOffice365PolicyProperties] 命令會定義要與虛擬裝置網站搭配使用的 Office 365 專題原則。</span><span class="sxs-lookup"><span data-stu-id="b79d7-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="b79d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="b79d7-107">EXAMPLES</span></span>

### <span data-ttu-id="b79d7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b79d7-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="b79d7-109">建立要與虛擬裝置網站命令搭配使用的 Office 365 流量排列原則物件。</span><span class="sxs-lookup"><span data-stu-id="b79d7-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="b79d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="b79d7-110">PARAMETERS</span></span>

### <span data-ttu-id="b79d7-111">-允許</span><span class="sxs-lookup"><span data-stu-id="b79d7-111">-Allow</span></span>
<span data-ttu-id="b79d7-112">將 [允許] 類別流量分類。</span><span class="sxs-lookup"><span data-stu-id="b79d7-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="b79d7-113">-預設值</span><span class="sxs-lookup"><span data-stu-id="b79d7-113">-Default</span></span>
<span data-ttu-id="b79d7-114">將預設類別交通劃分成專題討論。</span><span class="sxs-lookup"><span data-stu-id="b79d7-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="b79d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79d7-115">-DefaultProfile</span></span>
<span data-ttu-id="b79d7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b79d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b79d7-117">-優化</span><span class="sxs-lookup"><span data-stu-id="b79d7-117">-Optimize</span></span>
<span data-ttu-id="b79d7-118">將 [優化] 類別流量分類。</span><span class="sxs-lookup"><span data-stu-id="b79d7-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="b79d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79d7-119">CommonParameters</span></span>
<span data-ttu-id="b79d7-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b79d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79d7-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b79d7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79d7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b79d7-122">INPUTS</span></span>

### <span data-ttu-id="b79d7-123">所有</span><span class="sxs-lookup"><span data-stu-id="b79d7-123">None</span></span>

## <span data-ttu-id="b79d7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b79d7-124">OUTPUTS</span></span>

### <span data-ttu-id="b79d7-125">PSOffice365PolicyProperties 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b79d7-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="b79d7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b79d7-126">NOTES</span></span>

## <span data-ttu-id="b79d7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b79d7-127">RELATED LINKS</span></span>
