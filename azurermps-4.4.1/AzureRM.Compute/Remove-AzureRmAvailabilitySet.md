---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 796000ac20ab887d4abd26039da2a111a19141ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449993"
---
# <span data-ttu-id="86672-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="86672-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="86672-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86672-102">SYNOPSIS</span></span>
<span data-ttu-id="86672-103">從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="86672-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86672-104">句法</span><span class="sxs-lookup"><span data-stu-id="86672-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86672-105">說明</span><span class="sxs-lookup"><span data-stu-id="86672-105">DESCRIPTION</span></span>
<span data-ttu-id="86672-106">**AzureRmAvailabilitySet** Cmdlet 會從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="86672-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="86672-107">示例</span><span class="sxs-lookup"><span data-stu-id="86672-107">EXAMPLES</span></span>

### <span data-ttu-id="86672-108">範例1：移除可用性集</span><span class="sxs-lookup"><span data-stu-id="86672-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="86672-109">這個命令會在名為 ResourceGroup11 的資源群組中移除一個名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="86672-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="86672-110">參數</span><span class="sxs-lookup"><span data-stu-id="86672-110">PARAMETERS</span></span>

### <span data-ttu-id="86672-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86672-111">-DefaultProfile</span></span>
<span data-ttu-id="86672-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86672-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86672-113">-Force</span><span class="sxs-lookup"><span data-stu-id="86672-113">-Force</span></span>
<span data-ttu-id="86672-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="86672-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86672-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="86672-115">-Name</span></span>
<span data-ttu-id="86672-116">可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="86672-116">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86672-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86672-117">-ResourceGroupName</span></span>
<span data-ttu-id="86672-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="86672-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86672-119">-確認</span><span class="sxs-lookup"><span data-stu-id="86672-119">-Confirm</span></span>
<span data-ttu-id="86672-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="86672-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86672-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86672-121">-WhatIf</span></span>
<span data-ttu-id="86672-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86672-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="86672-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86672-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86672-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86672-124">CommonParameters</span></span>
<span data-ttu-id="86672-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86672-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86672-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86672-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86672-127">輸入</span><span class="sxs-lookup"><span data-stu-id="86672-127">INPUTS</span></span>

## <span data-ttu-id="86672-128">輸出</span><span class="sxs-lookup"><span data-stu-id="86672-128">OUTPUTS</span></span>

## <span data-ttu-id="86672-129">筆記</span><span class="sxs-lookup"><span data-stu-id="86672-129">NOTES</span></span>

## <span data-ttu-id="86672-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="86672-130">RELATED LINKS</span></span>

[<span data-ttu-id="86672-131">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="86672-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="86672-132">新-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="86672-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


