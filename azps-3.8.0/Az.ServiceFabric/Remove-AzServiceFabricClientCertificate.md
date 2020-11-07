---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: dc9f7dfa26b350a5dadea4bfa3afb9ad832fa063
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957621"
---
# <span data-ttu-id="1cc28-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1cc28-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="1cc28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cc28-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc28-103">移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="1cc28-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="1cc28-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cc28-104">SYNTAX</span></span>

### <span data-ttu-id="1cc28-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="1cc28-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cc28-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="1cc28-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc28-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="1cc28-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc28-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="1cc28-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc28-109">說明</span><span class="sxs-lookup"><span data-stu-id="1cc28-109">DESCRIPTION</span></span>
<span data-ttu-id="1cc28-110">使用 [ **移除-AzServiceFabricClientCertificate** ] 移除用戶端憑證 (s) 或 [證書受領人] (s) 名稱 (s 的) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="1cc28-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="1cc28-111">示例</span><span class="sxs-lookup"><span data-stu-id="1cc28-111">EXAMPLES</span></span>

### <span data-ttu-id="1cc28-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1cc28-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="1cc28-113">這個命令會從群集中移除指紋為「5F3660C715EBBDA31DB1FFDCF508302348DE8E7A」的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="1cc28-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="1cc28-114">參數</span><span class="sxs-lookup"><span data-stu-id="1cc28-114">PARAMETERS</span></span>

### <span data-ttu-id="1cc28-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="1cc28-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="1cc28-116">指定只有系統管理員許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="1cc28-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="1cc28-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="1cc28-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="1cc28-118">指定用戶端公用名稱、issuer 指紋及驗證類型</span><span class="sxs-lookup"><span data-stu-id="1cc28-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="1cc28-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="1cc28-119">-CommonName</span></span>
<span data-ttu-id="1cc28-120">指定用戶端憑證公用名</span><span class="sxs-lookup"><span data-stu-id="1cc28-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="1cc28-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc28-121">-DefaultProfile</span></span>
<span data-ttu-id="1cc28-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cc28-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc28-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="1cc28-123">-IssuerThumbprint</span></span>
<span data-ttu-id="1cc28-124">指定用戶端憑證的頒發者指紋</span><span class="sxs-lookup"><span data-stu-id="1cc28-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="1cc28-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cc28-125">-Name</span></span>
<span data-ttu-id="1cc28-126">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="1cc28-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="1cc28-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="1cc28-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="1cc28-128">指定只有 [唯讀] 許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="1cc28-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="1cc28-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc28-129">-ResourceGroupName</span></span>
<span data-ttu-id="1cc28-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc28-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1cc28-131">-指紋</span><span class="sxs-lookup"><span data-stu-id="1cc28-131">-Thumbprint</span></span>
<span data-ttu-id="1cc28-132">指定用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="1cc28-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="1cc28-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1cc28-133">-Confirm</span></span>
<span data-ttu-id="1cc28-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1cc28-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc28-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc28-135">-WhatIf</span></span>
<span data-ttu-id="1cc28-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cc28-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc28-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cc28-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc28-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc28-138">CommonParameters</span></span>
<span data-ttu-id="1cc28-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cc28-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc28-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cc28-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc28-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1cc28-141">INPUTS</span></span>

### <span data-ttu-id="1cc28-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1cc28-142">System.String</span></span>

### <span data-ttu-id="1cc28-143">System.object []</span><span class="sxs-lookup"><span data-stu-id="1cc28-143">System.String[]</span></span>

### <span data-ttu-id="1cc28-144">PSClientCertificateCommonName [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="1cc28-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="1cc28-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1cc28-145">OUTPUTS</span></span>

### <span data-ttu-id="1cc28-146">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="1cc28-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1cc28-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1cc28-147">NOTES</span></span>

## <span data-ttu-id="1cc28-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cc28-148">RELATED LINKS</span></span>

[<span data-ttu-id="1cc28-149">附加 AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1cc28-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
