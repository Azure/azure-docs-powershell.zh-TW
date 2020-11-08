---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128280"
---
# <span data-ttu-id="55da6-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="55da6-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="55da6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55da6-102">SYNOPSIS</span></span>
<span data-ttu-id="55da6-103">設定裝置的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="55da6-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="55da6-104">句法</span><span class="sxs-lookup"><span data-stu-id="55da6-104">SYNTAX</span></span>

### <span data-ttu-id="55da6-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="55da6-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55da6-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55da6-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55da6-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55da6-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55da6-108">說明</span><span class="sxs-lookup"><span data-stu-id="55da6-108">DESCRIPTION</span></span>
<span data-ttu-id="55da6-109">**AzDataBoxEdgeStorageAccountCredential** Cmdlet 會更新與資料盒 Edge 裝置上的儲存空間相對應的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="55da6-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="55da6-110">示例</span><span class="sxs-lookup"><span data-stu-id="55da6-110">EXAMPLES</span></span>

### <span data-ttu-id="55da6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="55da6-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="55da6-112">協助您旋轉儲存空間帳戶的存取鍵</span><span class="sxs-lookup"><span data-stu-id="55da6-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="55da6-113">參數</span><span class="sxs-lookup"><span data-stu-id="55da6-113">PARAMETERS</span></span>

### <span data-ttu-id="55da6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55da6-114">-AsJob</span></span>
<span data-ttu-id="55da6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="55da6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55da6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55da6-116">-DefaultProfile</span></span>
<span data-ttu-id="55da6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55da6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55da6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="55da6-118">-DeviceName</span></span>
<span data-ttu-id="55da6-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="55da6-119">Device Name</span></span>

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

### <span data-ttu-id="55da6-120">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="55da6-120">-EncryptionKey</span></span>
<span data-ttu-id="55da6-121">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="55da6-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="55da6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55da6-122">-InputObject</span></span>
<span data-ttu-id="55da6-123">輸入物件</span><span class="sxs-lookup"><span data-stu-id="55da6-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55da6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="55da6-124">-Name</span></span>
<span data-ttu-id="55da6-125">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="55da6-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55da6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55da6-126">-ResourceGroupName</span></span>
<span data-ttu-id="55da6-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="55da6-127">Resource Group Name</span></span>

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

### <span data-ttu-id="55da6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55da6-128">-ResourceId</span></span>
<span data-ttu-id="55da6-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="55da6-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="55da6-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="55da6-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="55da6-131">提供儲存空間帳戶存取金鑰</span><span class="sxs-lookup"><span data-stu-id="55da6-131">provide storage account access key</span></span>

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

### <span data-ttu-id="55da6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="55da6-132">-Confirm</span></span>
<span data-ttu-id="55da6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55da6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55da6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55da6-134">-WhatIf</span></span>
<span data-ttu-id="55da6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55da6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55da6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55da6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55da6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55da6-137">CommonParameters</span></span>
<span data-ttu-id="55da6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55da6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55da6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55da6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55da6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="55da6-140">INPUTS</span></span>

### <span data-ttu-id="55da6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="55da6-141">System.String</span></span>

### <span data-ttu-id="55da6-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="55da6-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="55da6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="55da6-143">OUTPUTS</span></span>

### <span data-ttu-id="55da6-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="55da6-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="55da6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="55da6-145">NOTES</span></span>

## <span data-ttu-id="55da6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="55da6-146">RELATED LINKS</span></span>