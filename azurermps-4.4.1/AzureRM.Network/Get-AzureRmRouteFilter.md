---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 80887622c5a9dbc3c6ddf544d435974b8212d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624210"
---
# <span data-ttu-id="f5081-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f5081-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="f5081-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5081-102">SYNOPSIS</span></span>
<span data-ttu-id="f5081-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="f5081-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5081-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5081-104">SYNTAX</span></span>

### <span data-ttu-id="f5081-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="f5081-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5081-106">擴充</span><span class="sxs-lookup"><span data-stu-id="f5081-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5081-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5081-107">DESCRIPTION</span></span>
<span data-ttu-id="f5081-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="f5081-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f5081-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5081-109">EXAMPLES</span></span>

### <span data-ttu-id="f5081-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f5081-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f5081-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="f5081-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f5081-112">參數</span><span class="sxs-lookup"><span data-stu-id="f5081-112">PARAMETERS</span></span>

### <span data-ttu-id="f5081-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f5081-113">-ExpandResource</span></span>
<span data-ttu-id="f5081-114">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="f5081-114">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5081-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5081-115">-Name</span></span>
<span data-ttu-id="f5081-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f5081-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5081-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5081-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5081-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5081-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5081-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5081-119">-DefaultProfile</span></span>
<span data-ttu-id="f5081-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5081-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5081-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5081-121">CommonParameters</span></span>
<span data-ttu-id="f5081-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5081-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5081-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5081-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5081-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f5081-124">INPUTS</span></span>

### <span data-ttu-id="f5081-125">System.object</span><span class="sxs-lookup"><span data-stu-id="f5081-125">System.String</span></span>

## <span data-ttu-id="f5081-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f5081-126">OUTPUTS</span></span>

### <span data-ttu-id="f5081-127">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5081-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f5081-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f5081-128">NOTES</span></span>

## <span data-ttu-id="f5081-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5081-129">RELATED LINKS</span></span>

