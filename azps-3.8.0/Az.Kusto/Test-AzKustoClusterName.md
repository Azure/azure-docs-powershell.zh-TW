---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: c6b2f462ac66ab48b50e7555a3b5bf7c844aae3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957057"
---
# <span data-ttu-id="a3c1f-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="a3c1f-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="a3c1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c1f-103">檢查指定的 Kusto 群集名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="a3c1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3c1f-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3c1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="a3c1f-106">檢查指定的 Kusto 群集名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="a3c1f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a3c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="a3c1f-108">範例 1-檢查使用中的 Kusto 群集名稱是否有空？</span><span class="sxs-lookup"><span data-stu-id="a3c1f-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="a3c1f-109">上述命令會傳回名為 "mykustocluster" 的 Kusto 群集是否存在於「美國中部」區域中。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="a3c1f-110">範例 2-檢查是否有空使用中的 Kusto 群集名稱</span><span class="sxs-lookup"><span data-stu-id="a3c1f-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="a3c1f-111">上述命令會傳回名為 "mykustocluster" 的 Kusto 群集是否存在於「美國中部」區域中。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="a3c1f-112">參數</span><span class="sxs-lookup"><span data-stu-id="a3c1f-112">PARAMETERS</span></span>

### <span data-ttu-id="a3c1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c1f-113">-DefaultProfile</span></span>
<span data-ttu-id="a3c1f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c1f-115">-位置</span><span class="sxs-lookup"><span data-stu-id="a3c1f-115">-Location</span></span>
<span data-ttu-id="a3c1f-116">要檢查的位置。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-116">The location where to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3c1f-117">-Name</span></span>
<span data-ttu-id="a3c1f-118">特定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-118">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c1f-119">CommonParameters</span></span>
<span data-ttu-id="a3c1f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c1f-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c1f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a3c1f-122">INPUTS</span></span>

### <span data-ttu-id="a3c1f-123">所有</span><span class="sxs-lookup"><span data-stu-id="a3c1f-123">None</span></span>

## <span data-ttu-id="a3c1f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a3c1f-124">OUTPUTS</span></span>

### <span data-ttu-id="a3c1f-125">PSKustoClusterNameAvailability 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="a3c1f-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="a3c1f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a3c1f-126">NOTES</span></span>

## <span data-ttu-id="a3c1f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3c1f-127">RELATED LINKS</span></span>
