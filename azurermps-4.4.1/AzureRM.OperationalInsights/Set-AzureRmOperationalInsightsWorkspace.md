---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446697"
---
# <span data-ttu-id="10a88-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="10a88-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="10a88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10a88-102">SYNOPSIS</span></span>
<span data-ttu-id="10a88-103">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="10a88-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10a88-104">句法</span><span class="sxs-lookup"><span data-stu-id="10a88-104">SYNTAX</span></span>

### <span data-ttu-id="10a88-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="10a88-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10a88-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="10a88-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10a88-107">說明</span><span class="sxs-lookup"><span data-stu-id="10a88-107">DESCRIPTION</span></span>
<span data-ttu-id="10a88-108">AzureRmOperationalInsightsWorkspace Cmdlet 會變更工作區的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="10a88-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="10a88-109">示例</span><span class="sxs-lookup"><span data-stu-id="10a88-109">EXAMPLES</span></span>

### <span data-ttu-id="10a88-110">範例1：依名稱修改工作區</span><span class="sxs-lookup"><span data-stu-id="10a88-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="10a88-111">這個命令會修改名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的 SKU 及標記。</span><span class="sxs-lookup"><span data-stu-id="10a88-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="10a88-112">範例2：使用管線更新工作區</span><span class="sxs-lookup"><span data-stu-id="10a88-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="10a88-113">這個命令會使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkSpace 的工作區，然後使用管線運算子將 SKU 傳送到 **AzureRmOperationalInsightsWorkspace** Cmdlet，以將 SKU 設定為 Premium。</span><span class="sxs-lookup"><span data-stu-id="10a88-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="10a88-114">參數</span><span class="sxs-lookup"><span data-stu-id="10a88-114">PARAMETERS</span></span>

### <span data-ttu-id="10a88-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="10a88-115">-Name</span></span>
<span data-ttu-id="10a88-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="10a88-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a88-117">-ResourceGroupName</span></span>
<span data-ttu-id="10a88-118">指定 Azure 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="10a88-118">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a88-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="10a88-119">-Sku</span></span>
<span data-ttu-id="10a88-120">指定工作區的服務層級。</span><span class="sxs-lookup"><span data-stu-id="10a88-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="10a88-121">有效值為：</span><span class="sxs-lookup"><span data-stu-id="10a88-121">Valid values are:</span></span> 

- <span data-ttu-id="10a88-122">空閒</span><span class="sxs-lookup"><span data-stu-id="10a88-122">free</span></span>
- <span data-ttu-id="10a88-123">標準</span><span class="sxs-lookup"><span data-stu-id="10a88-123">standard</span></span>
- <span data-ttu-id="10a88-124">佳</span><span class="sxs-lookup"><span data-stu-id="10a88-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a88-125">-標記</span><span class="sxs-lookup"><span data-stu-id="10a88-125">-Tags</span></span>
<span data-ttu-id="10a88-126">指定工作區的資源標記。</span><span class="sxs-lookup"><span data-stu-id="10a88-126">Specifies the resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a88-127">-工作區</span><span class="sxs-lookup"><span data-stu-id="10a88-127">-Workspace</span></span>
<span data-ttu-id="10a88-128">指定要更新的工作區。</span><span class="sxs-lookup"><span data-stu-id="10a88-128">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10a88-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a88-129">-DefaultProfile</span></span>
<span data-ttu-id="10a88-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10a88-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a88-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="10a88-131">-RetentionInDays</span></span>
<span data-ttu-id="10a88-132">工作區資料保留天數（天）。</span><span class="sxs-lookup"><span data-stu-id="10a88-132">The workspace data retention in days.</span></span> <span data-ttu-id="10a88-133">730 days 是所有其他 Sku 所允許的最大值。</span><span class="sxs-lookup"><span data-stu-id="10a88-133">730 days is the maximum allowed for all other Skus.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a88-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a88-134">CommonParameters</span></span>
<span data-ttu-id="10a88-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10a88-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a88-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10a88-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a88-137">輸入</span><span class="sxs-lookup"><span data-stu-id="10a88-137">INPUTS</span></span>

### <span data-ttu-id="10a88-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="10a88-138">PSWorkspace</span></span>
<span data-ttu-id="10a88-139">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="10a88-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="10a88-140">輸出</span><span class="sxs-lookup"><span data-stu-id="10a88-140">OUTPUTS</span></span>

### <span data-ttu-id="10a88-141">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="10a88-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="10a88-142">筆記</span><span class="sxs-lookup"><span data-stu-id="10a88-142">NOTES</span></span>

## <span data-ttu-id="10a88-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="10a88-143">RELATED LINKS</span></span>

[<span data-ttu-id="10a88-144">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="10a88-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="10a88-145">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="10a88-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


