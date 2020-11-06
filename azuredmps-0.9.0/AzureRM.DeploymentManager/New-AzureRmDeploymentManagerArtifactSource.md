---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: a6e69693d10adcb051ec8b33e35070f5c6656481
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442600"
---
# <span data-ttu-id="b7f6f-101">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7f6f-101">New-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b7f6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f6f-103">建立專案來源。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-103">Creates an artifact source.</span></span>

## <span data-ttu-id="b7f6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7f6f-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f6f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f6f-106">**新的-AzureRmDeploymentManagerArtifactSource** Cmdlet 會建立一個 [專案來源]。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-106">The **New-AzureRmDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="b7f6f-107">指定 *Name* 、 *ResourceGroupName* 和 required 屬性。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="b7f6f-108">您可以在本機修改傳回的物件，然後使用 Set-AzureRmDeploymentManagerArtifactSource Cmdlet 將變更套用至專案來源。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="b7f6f-109">這個 Cmdlet 會傳回 ArtifactSource 物件，其中包含可在 New-AzureRmDeloymentManagerServiceTopology Cmdlet 中參照的 ResourceId，所以 ServiceUnit 資源、範本和參數檔案所需的專案可以從這個位置參照。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzureRmDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="b7f6f-110">示例</span><span class="sxs-lookup"><span data-stu-id="b7f6f-110">EXAMPLES</span></span>

### <span data-ttu-id="b7f6f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b7f6f-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="b7f6f-112">在 ContosoResourceGroup 中建立具有名稱 ContosoArtifactSource 的專案來源，並將其設為資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="b7f6f-113">SasUri 屬性提供儲存工件之儲存容器的 Azure 儲存體 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="b7f6f-114">參數</span><span class="sxs-lookup"><span data-stu-id="b7f6f-114">PARAMETERS</span></span>

### <span data-ttu-id="b7f6f-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="b7f6f-115">-ArtifactRoot</span></span>
<span data-ttu-id="b7f6f-116">在專案的 [儲存] 容器下，選用的目錄位移。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-116">The optional directory offset under the storage container for the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f6f-117">-DefaultProfile</span></span>
<span data-ttu-id="b7f6f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f6f-119">-位置</span><span class="sxs-lookup"><span data-stu-id="b7f6f-119">-Location</span></span>
<span data-ttu-id="b7f6f-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-120">The location of the resource.</span></span>

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

### <span data-ttu-id="b7f6f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7f6f-121">-Name</span></span>
<span data-ttu-id="b7f6f-122">專案來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="b7f6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7f6f-124">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-124">The resource group.</span></span>

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

### <span data-ttu-id="b7f6f-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="b7f6f-125">-SasUri</span></span>
<span data-ttu-id="b7f6f-126">儲存工件之 Azure 儲存體容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="b7f6f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7f6f-127">-Tag</span></span>
<span data-ttu-id="b7f6f-128">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f6f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b7f6f-129">-Confirm</span></span>
<span data-ttu-id="b7f6f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f6f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f6f-131">-WhatIf</span></span>
<span data-ttu-id="b7f6f-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f6f-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f6f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f6f-134">CommonParameters</span></span>
<span data-ttu-id="b7f6f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f6f-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f6f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b7f6f-137">INPUTS</span></span>

### <span data-ttu-id="b7f6f-138">所有</span><span class="sxs-lookup"><span data-stu-id="b7f6f-138">None</span></span>

## <span data-ttu-id="b7f6f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b7f6f-139">OUTPUTS</span></span>

### <span data-ttu-id="b7f6f-140">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="b7f6f-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b7f6f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b7f6f-141">NOTES</span></span>

## <span data-ttu-id="b7f6f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7f6f-142">RELATED LINKS</span></span>

[<span data-ttu-id="b7f6f-143">AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7f6f-143">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="b7f6f-144">移除-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7f6f-144">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="b7f6f-145">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7f6f-145">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)