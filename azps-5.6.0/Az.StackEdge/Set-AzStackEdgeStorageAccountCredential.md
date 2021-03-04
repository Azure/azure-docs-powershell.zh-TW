---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 089979d2b571b7141758baf3f8d103a5a322bc28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913017"
---
# <span data-ttu-id="0ce33-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0ce33-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0ce33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ce33-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce33-103">設定裝置儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="0ce33-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="0ce33-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ce33-104">SYNTAX</span></span>

### <span data-ttu-id="0ce33-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0ce33-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce33-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ce33-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ce33-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ce33-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce33-108">描述</span><span class="sxs-lookup"><span data-stu-id="0ce33-108">DESCRIPTION</span></span>
<span data-ttu-id="0ce33-109">**Set-AzStackEdgeStorageAccountCredential Cmdlet** 會更新對應到 Stack Edge 裝置上儲存帳戶的儲存帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="0ce33-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="0ce33-110">例子</span><span class="sxs-lookup"><span data-stu-id="0ce33-110">EXAMPLES</span></span>

### <span data-ttu-id="0ce33-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0ce33-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="0ce33-112">協助旋轉儲存帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="0ce33-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="0ce33-113">參數</span><span class="sxs-lookup"><span data-stu-id="0ce33-113">PARAMETERS</span></span>

### <span data-ttu-id="0ce33-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ce33-114">-AsJob</span></span>
<span data-ttu-id="0ce33-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0ce33-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ce33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce33-116">-DefaultProfile</span></span>
<span data-ttu-id="0ce33-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ce33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce33-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0ce33-118">-DeviceName</span></span>
<span data-ttu-id="0ce33-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="0ce33-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0ce33-120">-EncryptionKey</span></span>
<span data-ttu-id="0ce33-121">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="0ce33-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce33-122">-InputObject</span></span>
<span data-ttu-id="0ce33-123">輸入物件</span><span class="sxs-lookup"><span data-stu-id="0ce33-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ce33-124">-Name</span></span>
<span data-ttu-id="0ce33-125">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="0ce33-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce33-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ce33-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="0ce33-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce33-128">-ResourceId</span></span>
<span data-ttu-id="0ce33-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce33-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="0ce33-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="0ce33-131">提供儲存空間帳戶訪問金鑰</span><span class="sxs-lookup"><span data-stu-id="0ce33-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ce33-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0ce33-132">-Confirm</span></span>
<span data-ttu-id="0ce33-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ce33-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce33-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce33-134">-WhatIf</span></span>
<span data-ttu-id="0ce33-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ce33-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ce33-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ce33-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce33-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce33-137">CommonParameters</span></span>
<span data-ttu-id="0ce33-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ce33-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce33-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ce33-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce33-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0ce33-140">INPUTS</span></span>

### <span data-ttu-id="0ce33-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0ce33-141">System.String</span></span>

### <span data-ttu-id="0ce33-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0ce33-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0ce33-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0ce33-143">OUTPUTS</span></span>

### <span data-ttu-id="0ce33-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0ce33-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0ce33-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0ce33-145">NOTES</span></span>

## <span data-ttu-id="0ce33-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ce33-146">RELATED LINKS</span></span>
