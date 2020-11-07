---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794367"
---
# <span data-ttu-id="a1a82-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a1a82-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="a1a82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1a82-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a82-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="a1a82-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="a1a82-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1a82-104">SYNTAX</span></span>

### <span data-ttu-id="a1a82-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="a1a82-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1a82-106">擴充</span><span class="sxs-lookup"><span data-stu-id="a1a82-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a82-107">說明</span><span class="sxs-lookup"><span data-stu-id="a1a82-107">DESCRIPTION</span></span>
<span data-ttu-id="a1a82-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="a1a82-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="a1a82-109">示例</span><span class="sxs-lookup"><span data-stu-id="a1a82-109">EXAMPLES</span></span>

### <span data-ttu-id="a1a82-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a1a82-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a1a82-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="a1a82-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="a1a82-112">參數</span><span class="sxs-lookup"><span data-stu-id="a1a82-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a82-113">-DefaultProfile</span></span>
<span data-ttu-id="a1a82-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1a82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a82-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a1a82-115">-ExpandResource</span></span>
<span data-ttu-id="a1a82-116">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="a1a82-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a82-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1a82-117">-Name</span></span>
<span data-ttu-id="a1a82-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a1a82-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a82-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1a82-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1a82-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a82-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a82-121">CommonParameters</span></span>
<span data-ttu-id="a1a82-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1a82-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a82-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1a82-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a82-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a1a82-124">INPUTS</span></span>

### <span data-ttu-id="a1a82-125">System.object</span><span class="sxs-lookup"><span data-stu-id="a1a82-125">System.String</span></span>

## <span data-ttu-id="a1a82-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a1a82-126">OUTPUTS</span></span>

### <span data-ttu-id="a1a82-127">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1a82-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a1a82-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a1a82-128">NOTES</span></span>

## <span data-ttu-id="a1a82-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1a82-129">RELATED LINKS</span></span>

