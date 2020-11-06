---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 6fe4d0c3a32cd96693d64e46f9d8596083dd9c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447969"
---
# <span data-ttu-id="61bb5-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="61bb5-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="61bb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="61bb5-103">從群集中移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="61bb5-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61bb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="61bb5-104">SYNTAX</span></span>

### <span data-ttu-id="61bb5-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="61bb5-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bb5-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="61bb5-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bb5-107">說明</span><span class="sxs-lookup"><span data-stu-id="61bb5-107">DESCRIPTION</span></span>
<span data-ttu-id="61bb5-108">使用 **移除-AzureRmServiceFabricSetting** 從群集中移除 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="61bb5-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="61bb5-109">示例</span><span class="sxs-lookup"><span data-stu-id="61bb5-109">EXAMPLES</span></span>

### <span data-ttu-id="61bb5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="61bb5-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="61bb5-111">此命令會移除 [EseStore] 區段下的 [MaxCursors] 設定。</span><span class="sxs-lookup"><span data-stu-id="61bb5-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="61bb5-112">參數</span><span class="sxs-lookup"><span data-stu-id="61bb5-112">PARAMETERS</span></span>

### <span data-ttu-id="61bb5-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="61bb5-113">-Name</span></span>
<span data-ttu-id="61bb5-114">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="61bb5-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="61bb5-115">-參數</span><span class="sxs-lookup"><span data-stu-id="61bb5-115">-Parameter</span></span>
<span data-ttu-id="61bb5-116">參數.</span><span class="sxs-lookup"><span data-stu-id="61bb5-116">Parameter.</span></span>

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

### <span data-ttu-id="61bb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="61bb5-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61bb5-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="61bb5-119">區段</span><span class="sxs-lookup"><span data-stu-id="61bb5-119">-Section</span></span>
<span data-ttu-id="61bb5-120">頂部.</span><span class="sxs-lookup"><span data-stu-id="61bb5-120">Section.</span></span>

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

### <span data-ttu-id="61bb5-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="61bb5-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="61bb5-122">用戶端驗證類型。</span><span class="sxs-lookup"><span data-stu-id="61bb5-122">Client authentication type.</span></span>

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

### <span data-ttu-id="61bb5-123">-確認</span><span class="sxs-lookup"><span data-stu-id="61bb5-123">-Confirm</span></span>
<span data-ttu-id="61bb5-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61bb5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bb5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bb5-125">-WhatIf</span></span>
<span data-ttu-id="61bb5-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61bb5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61bb5-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61bb5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bb5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bb5-128">-DefaultProfile</span></span>
<span data-ttu-id="61bb5-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61bb5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61bb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bb5-130">CommonParameters</span></span>
<span data-ttu-id="61bb5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61bb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bb5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61bb5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bb5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="61bb5-133">INPUTS</span></span>

### <span data-ttu-id="61bb5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="61bb5-134">System.String</span></span>
<span data-ttu-id="61bb5-135">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="61bb5-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="61bb5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="61bb5-136">OUTPUTS</span></span>

### <span data-ttu-id="61bb5-137">PsCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="61bb5-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="61bb5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="61bb5-138">NOTES</span></span>

## <span data-ttu-id="61bb5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="61bb5-139">RELATED LINKS</span></span>

