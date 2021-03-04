---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 1ed5b95346ffde947366696f30e54cfddcdea4d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915837"
---
# <span data-ttu-id="a965e-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a965e-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a965e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a965e-102">SYNOPSIS</span></span>
<span data-ttu-id="a965e-103">移除用戶端憑證 () 或憑證 () 名稱 () ，以用於用戶端驗證至該組。</span><span class="sxs-lookup"><span data-stu-id="a965e-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a965e-104">語法</span><span class="sxs-lookup"><span data-stu-id="a965e-104">SYNTAX</span></span>

### <span data-ttu-id="a965e-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a965e-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a965e-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a965e-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a965e-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a965e-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a965e-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a965e-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a965e-109">描述</span><span class="sxs-lookup"><span data-stu-id="a965e-109">DESCRIPTION</span></span>
<span data-ttu-id="a965e-110">使用 **Remove-AzServiceFabricClientCertificate** 移除用戶端憑證 (s) 或憑證主體 (的) 名稱 (s) ，以用於用戶端驗證至該組組。</span><span class="sxs-lookup"><span data-stu-id="a965e-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a965e-111">例子</span><span class="sxs-lookup"><span data-stu-id="a965e-111">EXAMPLES</span></span>

### <span data-ttu-id="a965e-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a965e-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a965e-113">此命令會從組塊移除具有指紋 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' 的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a965e-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="a965e-114">參數</span><span class="sxs-lookup"><span data-stu-id="a965e-114">PARAMETERS</span></span>

### <span data-ttu-id="a965e-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a965e-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="a965e-116">指定只有系統管理員許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="a965e-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="a965e-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a965e-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a965e-118">指定用戶端常用名稱、發行者指紋和驗證類型</span><span class="sxs-lookup"><span data-stu-id="a965e-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="a965e-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a965e-119">-CommonName</span></span>
<span data-ttu-id="a965e-120">指定用戶端憑證通用名稱</span><span class="sxs-lookup"><span data-stu-id="a965e-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="a965e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a965e-121">-DefaultProfile</span></span>
<span data-ttu-id="a965e-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a965e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a965e-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a965e-123">-IssuerThumbprint</span></span>
<span data-ttu-id="a965e-124">指定用戶端憑證發行者指紋</span><span class="sxs-lookup"><span data-stu-id="a965e-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="a965e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a965e-125">-Name</span></span>
<span data-ttu-id="a965e-126">指定組名</span><span class="sxs-lookup"><span data-stu-id="a965e-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a965e-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a965e-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a965e-128">指定只有唯讀許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="a965e-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="a965e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a965e-129">-ResourceGroupName</span></span>
<span data-ttu-id="a965e-130">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a965e-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a965e-131">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="a965e-131">-Thumbprint</span></span>
<span data-ttu-id="a965e-132">指定用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="a965e-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="a965e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a965e-133">-Confirm</span></span>
<span data-ttu-id="a965e-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a965e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a965e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a965e-135">-WhatIf</span></span>
<span data-ttu-id="a965e-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a965e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a965e-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a965e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a965e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a965e-138">CommonParameters</span></span>
<span data-ttu-id="a965e-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a965e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a965e-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a965e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a965e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a965e-141">INPUTS</span></span>

### <span data-ttu-id="a965e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a965e-142">System.String</span></span>

### <span data-ttu-id="a965e-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a965e-143">System.String[]</span></span>

### <span data-ttu-id="a965e-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="a965e-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="a965e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a965e-145">OUTPUTS</span></span>

### <span data-ttu-id="a965e-146">Microsoft.Azure.Commands.ServiceFabric.models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a965e-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a965e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a965e-147">NOTES</span></span>

## <span data-ttu-id="a965e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a965e-148">RELATED LINKS</span></span>

[<span data-ttu-id="a965e-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a965e-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
