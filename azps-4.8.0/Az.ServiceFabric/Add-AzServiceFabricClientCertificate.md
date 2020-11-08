---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127323"
---
# <span data-ttu-id="a3962-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a3962-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a3962-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3962-102">SYNOPSIS</span></span>
<span data-ttu-id="a3962-103">在群集中加入通用名稱或指紋，以進行用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="a3962-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a3962-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3962-104">SYNTAX</span></span>

### <span data-ttu-id="a3962-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a3962-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3962-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a3962-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3962-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a3962-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3962-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a3962-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3962-109">說明</span><span class="sxs-lookup"><span data-stu-id="a3962-109">DESCRIPTION</span></span>
<span data-ttu-id="a3962-110">使用 [ **載入 AzServiceFabricClientCertificate** ]，將通用名稱和頒發者指紋或憑證指紋新增至群集，以便用戶端可以使用它進行驗證。</span><span class="sxs-lookup"><span data-stu-id="a3962-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="a3962-111">示例</span><span class="sxs-lookup"><span data-stu-id="a3962-111">EXAMPLES</span></span>

### <span data-ttu-id="a3962-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a3962-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="a3962-113">這個命令會將指紋為「5F3660C715EBBDA31DB1FFDCF508302348DE8E7A」的憑證新增至群集，因此用戶端可以使用憑證作為系統管理員來與群集進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a3962-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="a3962-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a3962-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a3962-115">這個命令會將 [通用名稱] 為 "Contoso.com" 且頒發者指紋為 "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" 的唯讀用戶端憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="a3962-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="a3962-116">參數</span><span class="sxs-lookup"><span data-stu-id="a3962-116">PARAMETERS</span></span>

### <span data-ttu-id="a3962-117">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="a3962-117">-Admin</span></span>
<span data-ttu-id="a3962-118">用戶端驗證類型</span><span class="sxs-lookup"><span data-stu-id="a3962-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3962-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a3962-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="a3962-120">指定只有系統管理員許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="a3962-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="a3962-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a3962-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a3962-122">指定用戶端公用名稱、issuer 指紋及驗證類型</span><span class="sxs-lookup"><span data-stu-id="a3962-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="a3962-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a3962-123">-CommonName</span></span>
<span data-ttu-id="a3962-124">指定用戶端憑證公用名</span><span class="sxs-lookup"><span data-stu-id="a3962-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="a3962-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3962-125">-DefaultProfile</span></span>
<span data-ttu-id="a3962-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3962-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3962-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a3962-127">-IssuerThumbprint</span></span>
<span data-ttu-id="a3962-128">指定用戶端憑證的頒發者指紋</span><span class="sxs-lookup"><span data-stu-id="a3962-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="a3962-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3962-129">-Name</span></span>
<span data-ttu-id="a3962-130">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="a3962-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a3962-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a3962-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a3962-132">指定只有 [唯讀] 許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="a3962-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="a3962-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3962-133">-ResourceGroupName</span></span>
<span data-ttu-id="a3962-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3962-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a3962-135">-指紋</span><span class="sxs-lookup"><span data-stu-id="a3962-135">-Thumbprint</span></span>
<span data-ttu-id="a3962-136">指定用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="a3962-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="a3962-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a3962-137">-Confirm</span></span>
<span data-ttu-id="a3962-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3962-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3962-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3962-139">-WhatIf</span></span>
<span data-ttu-id="a3962-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3962-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3962-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3962-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3962-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3962-142">CommonParameters</span></span>
<span data-ttu-id="a3962-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3962-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3962-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3962-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3962-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a3962-145">INPUTS</span></span>

### <span data-ttu-id="a3962-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a3962-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a3962-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a3962-147">System.String</span></span>

### <span data-ttu-id="a3962-148">System.object []</span><span class="sxs-lookup"><span data-stu-id="a3962-148">System.String[]</span></span>

### <span data-ttu-id="a3962-149">PSClientCertificateCommonName [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="a3962-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="a3962-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a3962-150">OUTPUTS</span></span>

### <span data-ttu-id="a3962-151">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a3962-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a3962-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a3962-152">NOTES</span></span>

## <span data-ttu-id="a3962-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3962-153">RELATED LINKS</span></span>

[<span data-ttu-id="a3962-154">移除-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a3962-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)