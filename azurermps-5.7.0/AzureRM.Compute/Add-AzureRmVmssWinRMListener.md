---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444755"
---
# <span data-ttu-id="108ef-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="108ef-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="108ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="108ef-102">SYNOPSIS</span></span>
<span data-ttu-id="108ef-103">將 WinRM 偵聽程式新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="108ef-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="108ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="108ef-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108ef-105">說明</span><span class="sxs-lookup"><span data-stu-id="108ef-105">DESCRIPTION</span></span>
<span data-ttu-id="108ef-106">**AzureRmVmssWinRMListener** Cmdlet 會在虛擬機器縮放集 (VMSS) 上新增 Windows 遠端系統管理 (WinRM) 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="108ef-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="108ef-107">示例</span><span class="sxs-lookup"><span data-stu-id="108ef-107">EXAMPLES</span></span>

### <span data-ttu-id="108ef-108">範例1：將 WinRM 偵聽程式新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="108ef-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="108ef-109">這個範例會將 WinRM 監聽程式新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="108ef-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="108ef-110">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="108ef-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="108ef-111">第二個命令會將 HTTP 通訊協定 WinRM 偵聽程式新增至 VMSS 指定 URL 的憑證。</span><span class="sxs-lookup"><span data-stu-id="108ef-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="108ef-112">參數</span><span class="sxs-lookup"><span data-stu-id="108ef-112">PARAMETERS</span></span>

### <span data-ttu-id="108ef-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="108ef-113">-CertificateUrl</span></span>
<span data-ttu-id="108ef-114">指定提供新虛擬機器之憑證的連結（作為 URL）。</span><span class="sxs-lookup"><span data-stu-id="108ef-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108ef-115">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="108ef-115">-Protocol</span></span>
<span data-ttu-id="108ef-116">指定 WinRM 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="108ef-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="108ef-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="108ef-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="108ef-118">Http</span><span class="sxs-lookup"><span data-stu-id="108ef-118">Http</span></span>
- <span data-ttu-id="108ef-119">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="108ef-119">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108ef-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="108ef-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="108ef-121">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="108ef-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="108ef-122">您可以使用 New-AzureRmVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="108ef-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="108ef-123">-確認</span><span class="sxs-lookup"><span data-stu-id="108ef-123">-Confirm</span></span>
<span data-ttu-id="108ef-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="108ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="108ef-125">-WhatIf</span></span>
<span data-ttu-id="108ef-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="108ef-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="108ef-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="108ef-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108ef-128">CommonParameters</span></span>
<span data-ttu-id="108ef-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="108ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108ef-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="108ef-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108ef-131">輸入</span><span class="sxs-lookup"><span data-stu-id="108ef-131">INPUTS</span></span>

### <span data-ttu-id="108ef-132">所有</span><span class="sxs-lookup"><span data-stu-id="108ef-132">None</span></span>
<span data-ttu-id="108ef-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="108ef-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="108ef-134">輸出</span><span class="sxs-lookup"><span data-stu-id="108ef-134">OUTPUTS</span></span>

### <span data-ttu-id="108ef-135">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="108ef-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="108ef-136">筆記</span><span class="sxs-lookup"><span data-stu-id="108ef-136">NOTES</span></span>

## <span data-ttu-id="108ef-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="108ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="108ef-138">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="108ef-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


