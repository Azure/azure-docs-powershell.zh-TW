---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449197"
---
# <span data-ttu-id="e8338-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8338-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="e8338-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8338-102">SYNOPSIS</span></span>
<span data-ttu-id="e8338-103">更新資料工廠的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8338-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8338-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8338-104">SYNTAX</span></span>

### <span data-ttu-id="e8338-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="e8338-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8338-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8338-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8338-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8338-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8338-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8338-108">DESCRIPTION</span></span>
<span data-ttu-id="e8338-109">**AzureRmDataFactoryV2** Cmdlet 會更新資料工廠的標記或身分識別屬性。</span><span class="sxs-lookup"><span data-stu-id="e8338-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="e8338-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8338-110">EXAMPLES</span></span>

### <span data-ttu-id="e8338-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8338-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="e8338-112">這個命令會將工廠 WikiADF 的標籤更新為字典，其中包含名為 myNewTagName 且值為 myTagValue 的標記。</span><span class="sxs-lookup"><span data-stu-id="e8338-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="e8338-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8338-113">PARAMETERS</span></span>

### <span data-ttu-id="e8338-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8338-114">-DefaultProfile</span></span>
<span data-ttu-id="e8338-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8338-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8338-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8338-116">-InputObject</span></span>
<span data-ttu-id="e8338-117">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="e8338-117">The data factory object.</span></span>

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

### <span data-ttu-id="e8338-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8338-118">-Name</span></span>
<span data-ttu-id="e8338-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e8338-119">The data factory name.</span></span>

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

### <span data-ttu-id="e8338-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8338-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8338-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8338-121">The resource group name.</span></span>

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

### <span data-ttu-id="e8338-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8338-122">-ResourceId</span></span>
<span data-ttu-id="e8338-123">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8338-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e8338-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8338-124">-Tag</span></span>
<span data-ttu-id="e8338-125">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="e8338-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="e8338-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e8338-126">-Confirm</span></span>
<span data-ttu-id="e8338-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8338-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8338-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8338-128">-WhatIf</span></span>
<span data-ttu-id="e8338-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8338-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8338-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8338-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8338-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8338-131">CommonParameters</span></span>
<span data-ttu-id="e8338-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8338-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8338-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8338-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8338-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e8338-134">INPUTS</span></span>

### <span data-ttu-id="e8338-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8338-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="e8338-136">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e8338-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e8338-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e8338-137">System.String</span></span>

## <span data-ttu-id="e8338-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e8338-138">OUTPUTS</span></span>

### <span data-ttu-id="e8338-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8338-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e8338-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e8338-140">NOTES</span></span>

## <span data-ttu-id="e8338-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8338-141">RELATED LINKS</span></span>
