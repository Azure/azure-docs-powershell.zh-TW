---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d0ba19efaf0cf3dc1f997d06231e056fb20b02f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447975"
---
# <span data-ttu-id="f1775-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f1775-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="f1775-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1775-102">SYNOPSIS</span></span>
<span data-ttu-id="f1775-103">移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="f1775-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1775-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1775-104">SYNTAX</span></span>

### <span data-ttu-id="f1775-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="f1775-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1775-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="f1775-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1775-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="f1775-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1775-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="f1775-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1775-109">說明</span><span class="sxs-lookup"><span data-stu-id="f1775-109">DESCRIPTION</span></span>
<span data-ttu-id="f1775-110">使用 [ **移除-AzureRmServiceFabricClientCertificate** ] 移除用戶端憑證 (s) 或 [證書受領人] (s) 名稱 (s 的) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="f1775-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="f1775-111">示例</span><span class="sxs-lookup"><span data-stu-id="f1775-111">EXAMPLES</span></span>

### <span data-ttu-id="f1775-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f1775-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f1775-113">這個命令會從群集中移除指紋為「5F3660C715EBBDA31DB1FFDCF508302348DE8E7A」的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="f1775-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="f1775-114">參數</span><span class="sxs-lookup"><span data-stu-id="f1775-114">PARAMETERS</span></span>

### <span data-ttu-id="f1775-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="f1775-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="f1775-116">指定只有系統管理員許可權的用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="f1775-116">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="f1775-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="f1775-118">指定用戶端公用名稱、頒發者指紋及驗證類型。</span><span class="sxs-lookup"><span data-stu-id="f1775-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="f1775-119">-CommonName</span></span>
<span data-ttu-id="f1775-120">指定用戶端憑證公用名。</span><span class="sxs-lookup"><span data-stu-id="f1775-120">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-121">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f1775-121">-IssuerThumbprint</span></span>
<span data-ttu-id="f1775-122">指定用戶端憑證頒發者指紋。</span><span class="sxs-lookup"><span data-stu-id="f1775-122">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1775-123">-Name</span></span>
<span data-ttu-id="f1775-124">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1775-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f1775-125">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="f1775-125">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="f1775-126">指定擁有唯讀許可權的用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="f1775-126">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1775-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1775-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1775-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f1775-129">-指紋</span><span class="sxs-lookup"><span data-stu-id="f1775-129">-Thumbprint</span></span>
<span data-ttu-id="f1775-130">指定用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="f1775-130">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1775-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f1775-131">-Confirm</span></span>
<span data-ttu-id="f1775-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1775-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1775-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1775-133">-WhatIf</span></span>
<span data-ttu-id="f1775-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1775-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1775-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1775-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1775-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1775-136">-DefaultProfile</span></span>
<span data-ttu-id="f1775-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1775-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1775-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1775-138">CommonParameters</span></span>
<span data-ttu-id="f1775-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1775-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1775-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1775-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1775-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f1775-141">INPUTS</span></span>

### <span data-ttu-id="f1775-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1775-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="f1775-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f1775-143">System.String</span></span>

<span data-ttu-id="f1775-144">System.object</span><span class="sxs-lookup"><span data-stu-id="f1775-144">System.Boolean</span></span>

## <span data-ttu-id="f1775-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f1775-145">OUTPUTS</span></span>

### <span data-ttu-id="f1775-146">PsCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="f1775-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="f1775-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f1775-147">NOTES</span></span>

## <span data-ttu-id="f1775-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1775-148">RELATED LINKS</span></span>

[<span data-ttu-id="f1775-149">附加 AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f1775-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
