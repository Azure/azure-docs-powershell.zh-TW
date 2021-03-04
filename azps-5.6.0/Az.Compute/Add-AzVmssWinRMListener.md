---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 9e4c560021f03b2612d2b7d3bd60fd91a72aa53b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906290"
---
# <span data-ttu-id="a6750-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="a6750-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="a6750-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6750-102">SYNOPSIS</span></span>
<span data-ttu-id="a6750-103">將 WinRM 聆聽者新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="a6750-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="a6750-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6750-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6750-105">描述</span><span class="sxs-lookup"><span data-stu-id="a6750-105">DESCRIPTION</span></span>
<span data-ttu-id="a6750-106">**Add-Az VmssWinRMListener Cmdlet** 會新增 Windows 遠端系統管理 (WinRM) 在虛擬機器縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="a6750-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a6750-107">例子</span><span class="sxs-lookup"><span data-stu-id="a6750-107">EXAMPLES</span></span>

### <span data-ttu-id="a6750-108">範例 1：新增 WinRM 聆聽者至 VMSS</span><span class="sxs-lookup"><span data-stu-id="a6750-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="a6750-109">此範例會將 WinRM 聆聽者新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="a6750-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="a6750-110">第一個命令使用 **New-Az VmssConfig** Cmdlet 來建立 VMSS 組式物件，並儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="a6750-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a6750-111">第二個命令會將 HTTP 通訊協定 WinRM 聆聽者與憑證一起新增到 VMSS 的指定 URL。</span><span class="sxs-lookup"><span data-stu-id="a6750-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="a6750-112">參數</span><span class="sxs-lookup"><span data-stu-id="a6750-112">PARAMETERS</span></span>

### <span data-ttu-id="a6750-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a6750-113">-CertificateUrl</span></span>
<span data-ttu-id="a6750-114">指定要配置新虛擬機器之憑證的連結做為 URL。</span><span class="sxs-lookup"><span data-stu-id="a6750-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6750-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6750-115">-DefaultProfile</span></span>
<span data-ttu-id="a6750-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6750-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6750-117">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a6750-117">-Protocol</span></span>
<span data-ttu-id="a6750-118">指定 WinRM 聆聽者通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a6750-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="a6750-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a6750-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6750-120">HTTP</span><span class="sxs-lookup"><span data-stu-id="a6750-120">Http</span></span>
- <span data-ttu-id="a6750-121">Https</span><span class="sxs-lookup"><span data-stu-id="a6750-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6750-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6750-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a6750-123">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="a6750-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="a6750-124">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="a6750-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6750-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a6750-125">-Confirm</span></span>
<span data-ttu-id="a6750-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6750-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6750-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6750-127">-WhatIf</span></span>
<span data-ttu-id="a6750-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6750-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6750-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6750-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6750-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6750-130">CommonParameters</span></span>
<span data-ttu-id="a6750-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6750-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6750-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6750-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6750-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a6750-133">INPUTS</span></span>

### <span data-ttu-id="a6750-134">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6750-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a6750-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a6750-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a6750-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a6750-136">System.String</span></span>

## <span data-ttu-id="a6750-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a6750-137">OUTPUTS</span></span>

### <span data-ttu-id="a6750-138">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6750-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a6750-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a6750-139">NOTES</span></span>

## <span data-ttu-id="a6750-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6750-140">RELATED LINKS</span></span>

[<span data-ttu-id="a6750-141">New-AzEvssConfig</span><span class="sxs-lookup"><span data-stu-id="a6750-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


