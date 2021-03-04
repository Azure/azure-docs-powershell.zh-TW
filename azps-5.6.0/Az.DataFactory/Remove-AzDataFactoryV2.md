---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: 99033646aac6f41397a7097afc8d78626d905a95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916756"
---
# <span data-ttu-id="c648f-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c648f-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="c648f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c648f-102">SYNOPSIS</span></span>
<span data-ttu-id="c648f-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="c648f-103">Removes a data factory.</span></span>

## <span data-ttu-id="c648f-104">語法</span><span class="sxs-lookup"><span data-stu-id="c648f-104">SYNTAX</span></span>

### <span data-ttu-id="c648f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="c648f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c648f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c648f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c648f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c648f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c648f-108">描述</span><span class="sxs-lookup"><span data-stu-id="c648f-108">DESCRIPTION</span></span>
<span data-ttu-id="c648f-109">Cmdlet Remove-AzDataFactoryV2移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="c648f-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="c648f-110">例子</span><span class="sxs-lookup"><span data-stu-id="c648f-110">EXAMPLES</span></span>

### <span data-ttu-id="c648f-111">範例 1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="c648f-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="c648f-112">此命令會從名為 ADF 的資源群組移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="c648f-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="c648f-113">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="c648f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="c648f-114">參數</span><span class="sxs-lookup"><span data-stu-id="c648f-114">PARAMETERS</span></span>

### <span data-ttu-id="c648f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c648f-115">-DefaultProfile</span></span>
<span data-ttu-id="c648f-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c648f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c648f-117">-強制</span><span class="sxs-lookup"><span data-stu-id="c648f-117">-Force</span></span>
<span data-ttu-id="c648f-118">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="c648f-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c648f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c648f-119">-InputObject</span></span>
<span data-ttu-id="c648f-120">指定要移除的 DataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="c648f-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c648f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c648f-121">-Name</span></span>
<span data-ttu-id="c648f-122">指定要移除的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="c648f-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c648f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c648f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c648f-124">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c648f-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c648f-125">此 Cmdlet 會從此參數指定的群組移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="c648f-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c648f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c648f-126">-ResourceId</span></span>
<span data-ttu-id="c648f-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c648f-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c648f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c648f-128">-Confirm</span></span>
<span data-ttu-id="c648f-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c648f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c648f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c648f-130">-WhatIf</span></span>
<span data-ttu-id="c648f-131">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c648f-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c648f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c648f-132">CommonParameters</span></span>
<span data-ttu-id="c648f-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c648f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c648f-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c648f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c648f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c648f-135">INPUTS</span></span>

### <span data-ttu-id="c648f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c648f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="c648f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c648f-137">System.String</span></span>

## <span data-ttu-id="c648f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c648f-138">OUTPUTS</span></span>

### <span data-ttu-id="c648f-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="c648f-139">System.Void</span></span>

## <span data-ttu-id="c648f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c648f-140">NOTES</span></span>
<span data-ttu-id="c648f-141">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="c648f-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c648f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c648f-142">RELATED LINKS</span></span>

[<span data-ttu-id="c648f-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c648f-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="c648f-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c648f-144">Set-AzDataFactoryV2</span></span>]()
