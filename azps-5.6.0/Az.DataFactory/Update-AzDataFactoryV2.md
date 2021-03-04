---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: c80716e53b6f3aec6c9196baebbcd333aed1582c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905129"
---
# <span data-ttu-id="a60b1-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a60b1-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="a60b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a60b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a60b1-103">更新資料工廠的屬性。</span><span class="sxs-lookup"><span data-stu-id="a60b1-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="a60b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="a60b1-104">SYNTAX</span></span>

### <span data-ttu-id="a60b1-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a60b1-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a60b1-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a60b1-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60b1-108">描述</span><span class="sxs-lookup"><span data-stu-id="a60b1-108">DESCRIPTION</span></span>
<span data-ttu-id="a60b1-109">**Update-AzDataFactoryV2** Cmdlet 會更新資料工廠的標籤或身分識別屬性。</span><span class="sxs-lookup"><span data-stu-id="a60b1-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="a60b1-110">例子</span><span class="sxs-lookup"><span data-stu-id="a60b1-110">EXAMPLES</span></span>

### <span data-ttu-id="a60b1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a60b1-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="a60b1-112">此命令會更新工廠 WikiADF 的標記至字典，其中包含名為 myNewTagName 與值 myTagValue 的標記。</span><span class="sxs-lookup"><span data-stu-id="a60b1-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="a60b1-113">參數</span><span class="sxs-lookup"><span data-stu-id="a60b1-113">PARAMETERS</span></span>

### <span data-ttu-id="a60b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60b1-114">-DefaultProfile</span></span>
<span data-ttu-id="a60b1-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a60b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60b1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a60b1-116">-InputObject</span></span>
<span data-ttu-id="a60b1-117">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="a60b1-117">The data factory object.</span></span>

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

### <span data-ttu-id="a60b1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a60b1-118">-Name</span></span>
<span data-ttu-id="a60b1-119">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a60b1-119">The data factory name.</span></span>

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

### <span data-ttu-id="a60b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="a60b1-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a60b1-121">The resource group name.</span></span>

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

### <span data-ttu-id="a60b1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a60b1-122">-ResourceId</span></span>
<span data-ttu-id="a60b1-123">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a60b1-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a60b1-124">-標記</span><span class="sxs-lookup"><span data-stu-id="a60b1-124">-Tag</span></span>
<span data-ttu-id="a60b1-125">資料工廠的標記。</span><span class="sxs-lookup"><span data-stu-id="a60b1-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60b1-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a60b1-126">-Confirm</span></span>
<span data-ttu-id="a60b1-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a60b1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60b1-128">-WhatIf</span></span>
<span data-ttu-id="a60b1-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a60b1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a60b1-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a60b1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60b1-131">CommonParameters</span></span>
<span data-ttu-id="a60b1-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a60b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60b1-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a60b1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60b1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a60b1-134">INPUTS</span></span>

### <span data-ttu-id="a60b1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a60b1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="a60b1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a60b1-136">System.String</span></span>

## <span data-ttu-id="a60b1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a60b1-137">OUTPUTS</span></span>

### <span data-ttu-id="a60b1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a60b1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a60b1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a60b1-139">NOTES</span></span>

## <span data-ttu-id="a60b1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a60b1-140">RELATED LINKS</span></span>
