---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130623"
---
# <span data-ttu-id="ac573-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="ac573-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="ac573-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac573-102">SYNOPSIS</span></span>
<span data-ttu-id="ac573-103">移除裝置的儲存帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="ac573-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="ac573-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac573-104">SYNTAX</span></span>

### <span data-ttu-id="ac573-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ac573-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac573-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac573-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac573-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac573-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac573-108">說明</span><span class="sxs-lookup"><span data-stu-id="ac573-108">DESCRIPTION</span></span>
<span data-ttu-id="ac573-109">**AzStackEdgeStorageAccountCredential** Cmdlet 會移除堆疊 Edge 裝置的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="ac573-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="ac573-110">示例</span><span class="sxs-lookup"><span data-stu-id="ac573-110">EXAMPLES</span></span>

### <span data-ttu-id="ac573-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ac573-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="ac573-112">參數</span><span class="sxs-lookup"><span data-stu-id="ac573-112">PARAMETERS</span></span>

### <span data-ttu-id="ac573-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac573-113">-AsJob</span></span>
<span data-ttu-id="ac573-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac573-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac573-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac573-115">-DefaultProfile</span></span>
<span data-ttu-id="ac573-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac573-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac573-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ac573-117">-DeviceName</span></span>
<span data-ttu-id="ac573-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="ac573-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac573-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac573-119">-InputObject</span></span>
<span data-ttu-id="ac573-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="ac573-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac573-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac573-121">-Name</span></span>
<span data-ttu-id="ac573-122">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ac573-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac573-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac573-123">-PassThru</span></span>
<span data-ttu-id="ac573-124">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="ac573-124">returns true if successful</span></span>

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

### <span data-ttu-id="ac573-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac573-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac573-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ac573-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac573-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac573-127">-ResourceId</span></span>
<span data-ttu-id="ac573-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac573-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac573-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ac573-129">-Confirm</span></span>
<span data-ttu-id="ac573-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac573-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac573-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac573-131">-WhatIf</span></span>
<span data-ttu-id="ac573-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac573-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac573-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac573-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac573-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac573-134">CommonParameters</span></span>
<span data-ttu-id="ac573-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac573-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac573-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ac573-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac573-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ac573-137">INPUTS</span></span>

### <span data-ttu-id="ac573-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ac573-138">System.String</span></span>

### <span data-ttu-id="ac573-139">PSStackEdgeStorageAccountCredential （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="ac573-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="ac573-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ac573-140">OUTPUTS</span></span>

### <span data-ttu-id="ac573-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ac573-141">System.Boolean</span></span>

## <span data-ttu-id="ac573-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ac573-142">NOTES</span></span>

## <span data-ttu-id="ac573-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac573-143">RELATED LINKS</span></span>
