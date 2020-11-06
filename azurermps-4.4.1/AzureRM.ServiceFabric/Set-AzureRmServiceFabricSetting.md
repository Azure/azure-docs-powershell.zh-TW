---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: ef369f67e683a214538f1ecb113f771e2f5cd2f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447968"
---
# <span data-ttu-id="b100b-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b100b-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="b100b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b100b-102">SYNOPSIS</span></span>
<span data-ttu-id="b100b-103">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="b100b-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b100b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b100b-104">SYNTAX</span></span>

### <span data-ttu-id="b100b-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b100b-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b100b-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b100b-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b100b-107">說明</span><span class="sxs-lookup"><span data-stu-id="b100b-107">DESCRIPTION</span></span>
<span data-ttu-id="b100b-108">使用 [ **設定] AzureRmServiceFabricSetting** 在群集中新增或更新 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="b100b-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="b100b-109">示例</span><span class="sxs-lookup"><span data-stu-id="b100b-109">EXAMPLES</span></span>

### <span data-ttu-id="b100b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b100b-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="b100b-111">這個命令會將 [MaxFileOperationTimeout] 設定為「NamingService」區段下的值 ' 5000」。</span><span class="sxs-lookup"><span data-stu-id="b100b-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="b100b-112">參數</span><span class="sxs-lookup"><span data-stu-id="b100b-112">PARAMETERS</span></span>

### <span data-ttu-id="b100b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b100b-113">-Name</span></span>
<span data-ttu-id="b100b-114">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b100b-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b100b-115">-參數</span><span class="sxs-lookup"><span data-stu-id="b100b-115">-Parameter</span></span>
<span data-ttu-id="b100b-116">參數.</span><span class="sxs-lookup"><span data-stu-id="b100b-116">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b100b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b100b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b100b-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b100b-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b100b-119">區段</span><span class="sxs-lookup"><span data-stu-id="b100b-119">-Section</span></span>
<span data-ttu-id="b100b-120">頂部.</span><span class="sxs-lookup"><span data-stu-id="b100b-120">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b100b-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b100b-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="b100b-122">用戶端驗證類型。</span><span class="sxs-lookup"><span data-stu-id="b100b-122">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b100b-123">-值</span><span class="sxs-lookup"><span data-stu-id="b100b-123">-Value</span></span>
<span data-ttu-id="b100b-124">有效值.</span><span class="sxs-lookup"><span data-stu-id="b100b-124">Value.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b100b-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b100b-125">-Confirm</span></span>
<span data-ttu-id="b100b-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b100b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b100b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b100b-127">-WhatIf</span></span>
<span data-ttu-id="b100b-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b100b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b100b-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b100b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b100b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b100b-130">-DefaultProfile</span></span>
<span data-ttu-id="b100b-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b100b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b100b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b100b-132">CommonParameters</span></span>
<span data-ttu-id="b100b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b100b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b100b-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b100b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b100b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b100b-135">INPUTS</span></span>

### <span data-ttu-id="b100b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b100b-136">System.String</span></span>
<span data-ttu-id="b100b-137">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="b100b-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b100b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b100b-138">OUTPUTS</span></span>

### <span data-ttu-id="b100b-139">PsCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="b100b-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="b100b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b100b-140">NOTES</span></span>

## <span data-ttu-id="b100b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b100b-141">RELATED LINKS</span></span>

