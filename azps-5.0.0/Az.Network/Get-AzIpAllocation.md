---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139575"
---
# <span data-ttu-id="e93ce-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="e93ce-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="e93ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e93ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e93ce-103">取得 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="e93ce-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="e93ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="e93ce-104">SYNTAX</span></span>

### <span data-ttu-id="e93ce-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e93ce-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e93ce-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="e93ce-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e93ce-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e93ce-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e93ce-108">說明</span><span class="sxs-lookup"><span data-stu-id="e93ce-108">DESCRIPTION</span></span>
<span data-ttu-id="e93ce-109">**AzIpAllocation** Cmdlet 會取得 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="e93ce-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="e93ce-110">示例</span><span class="sxs-lookup"><span data-stu-id="e93ce-110">EXAMPLES</span></span>

### <span data-ttu-id="e93ce-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e93ce-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="e93ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="e93ce-112">PARAMETERS</span></span>

### <span data-ttu-id="e93ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93ce-113">-DefaultProfile</span></span>
<span data-ttu-id="e93ce-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e93ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e93ce-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e93ce-115">-Name</span></span>
<span data-ttu-id="e93ce-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e93ce-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e93ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="e93ce-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e93ce-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e93ce-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e93ce-119">-ResourceId</span></span>
<span data-ttu-id="e93ce-120">IpAllocation 識別碼</span><span class="sxs-lookup"><span data-stu-id="e93ce-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93ce-121">CommonParameters</span></span>
<span data-ttu-id="e93ce-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e93ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93ce-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e93ce-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93ce-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e93ce-124">INPUTS</span></span>

### <span data-ttu-id="e93ce-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e93ce-125">System.String</span></span>

## <span data-ttu-id="e93ce-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e93ce-126">OUTPUTS</span></span>

### <span data-ttu-id="e93ce-127">PSIpAllocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e93ce-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="e93ce-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e93ce-128">NOTES</span></span>

## <span data-ttu-id="e93ce-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e93ce-129">RELATED LINKS</span></span>
