---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 1d7655a78ee2abe00b69d485c35b73cee91ee420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624154"
---
# <span data-ttu-id="e0992-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="e0992-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="e0992-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0992-102">SYNOPSIS</span></span>
<span data-ttu-id="e0992-103">開始手動升級 VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="e0992-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0992-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0992-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0992-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0992-105">DESCRIPTION</span></span>
<span data-ttu-id="e0992-106">Update-AzureRmVmssInstance Cmdlet 會啟動手動升級指定的虛擬機器縮放集， (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="e0992-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="e0992-107">當 VMSS 縮放設定上的升級原則設定為 [手動] 時，就會使用這種情況。</span><span class="sxs-lookup"><span data-stu-id="e0992-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="e0992-108">示例</span><span class="sxs-lookup"><span data-stu-id="e0992-108">EXAMPLES</span></span>

### <span data-ttu-id="e0992-109">範例1：開始升級 VMSS 實例</span><span class="sxs-lookup"><span data-stu-id="e0992-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="e0992-110">這個命令會啟動實例識別碼為0的 VMSS 命名 VMScaleSet001。</span><span class="sxs-lookup"><span data-stu-id="e0992-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="e0992-111">參數</span><span class="sxs-lookup"><span data-stu-id="e0992-111">PARAMETERS</span></span>

### <span data-ttu-id="e0992-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0992-112">-DefaultProfile</span></span>
<span data-ttu-id="e0992-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0992-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0992-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e0992-114">-InstanceId</span></span>
<span data-ttu-id="e0992-115">指定作為字串陣列，即要升級之實例的識別碼或 Id。</span><span class="sxs-lookup"><span data-stu-id="e0992-115">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0992-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0992-116">-ResourceGroupName</span></span>
<span data-ttu-id="e0992-117">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0992-117">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0992-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e0992-118">-VMScaleSetName</span></span>
<span data-ttu-id="e0992-119">指定此 Cmdlet 升級之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0992-119">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0992-120">-確認</span><span class="sxs-lookup"><span data-stu-id="e0992-120">-Confirm</span></span>
<span data-ttu-id="e0992-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0992-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0992-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0992-122">-WhatIf</span></span>
<span data-ttu-id="e0992-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0992-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e0992-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0992-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0992-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0992-125">CommonParameters</span></span>
<span data-ttu-id="e0992-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0992-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0992-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0992-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0992-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e0992-128">INPUTS</span></span>

## <span data-ttu-id="e0992-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e0992-129">OUTPUTS</span></span>

###  
<span data-ttu-id="e0992-130">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e0992-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e0992-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e0992-131">NOTES</span></span>

## <span data-ttu-id="e0992-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0992-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0992-133">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0992-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


