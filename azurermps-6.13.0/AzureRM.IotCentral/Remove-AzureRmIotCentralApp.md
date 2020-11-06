---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457031"
---
# <span data-ttu-id="e7165-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e7165-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="e7165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7165-102">SYNOPSIS</span></span>
<span data-ttu-id="e7165-103">刪除 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="e7165-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7165-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7165-104">SYNTAX</span></span>

### <span data-ttu-id="e7165-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e7165-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7165-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7165-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7165-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7165-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7165-108">說明</span><span class="sxs-lookup"><span data-stu-id="e7165-108">DESCRIPTION</span></span>
<span data-ttu-id="e7165-109">刪除現有的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="e7165-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="e7165-110">示例</span><span class="sxs-lookup"><span data-stu-id="e7165-110">EXAMPLES</span></span>

### <span data-ttu-id="e7165-111">範例 1 Delete 和 IoT 中央應用程式</span><span class="sxs-lookup"><span data-stu-id="e7165-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="e7165-112">刪除提供的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="e7165-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="e7165-113">參數</span><span class="sxs-lookup"><span data-stu-id="e7165-113">PARAMETERS</span></span>

### <span data-ttu-id="e7165-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7165-114">-AsJob</span></span>
<span data-ttu-id="e7165-115">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="e7165-115">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7165-116">-DefaultProfile</span></span>
<span data-ttu-id="e7165-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7165-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7165-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7165-118">-InputObject</span></span>
<span data-ttu-id="e7165-119">Iot 中央應用程式輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e7165-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7165-120">-Name</span></span>
<span data-ttu-id="e7165-121">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7165-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7165-122">-PassThru</span></span>
<span data-ttu-id="e7165-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="e7165-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7165-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7165-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7165-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7165-126">-ResourceId</span></span>
<span data-ttu-id="e7165-127">Iot 中心應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7165-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e7165-128">-Confirm</span></span>
<span data-ttu-id="e7165-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7165-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7165-130">-WhatIf</span></span>
<span data-ttu-id="e7165-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7165-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7165-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7165-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7165-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7165-133">CommonParameters</span></span>
<span data-ttu-id="e7165-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7165-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7165-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7165-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7165-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e7165-136">INPUTS</span></span>

### <span data-ttu-id="e7165-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e7165-137">System.String</span></span>
### <span data-ttu-id="e7165-138">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="e7165-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="e7165-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e7165-139">OUTPUTS</span></span>

### <span data-ttu-id="e7165-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e7165-140">System.Boolean</span></span>
## <span data-ttu-id="e7165-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e7165-141">NOTES</span></span>

## <span data-ttu-id="e7165-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7165-142">RELATED LINKS</span></span>