---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 77cefdacfee2e2c8cb1e0d5508a418cf6bbafcbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456856"
---
# <span data-ttu-id="edf01-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="edf01-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="edf01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edf01-102">SYNOPSIS</span></span>
<span data-ttu-id="edf01-103">將 WinRM 偵聽程式新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="edf01-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edf01-104">句法</span><span class="sxs-lookup"><span data-stu-id="edf01-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edf01-105">說明</span><span class="sxs-lookup"><span data-stu-id="edf01-105">DESCRIPTION</span></span>
<span data-ttu-id="edf01-106">**AzureRmVmssWinRMListener** Cmdlet 會在虛擬機器縮放集 (VMSS) 上新增 Windows 遠端系統管理 (WinRM) 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="edf01-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="edf01-107">示例</span><span class="sxs-lookup"><span data-stu-id="edf01-107">EXAMPLES</span></span>

### <span data-ttu-id="edf01-108">範例1：將 WinRM 偵聽程式新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="edf01-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="edf01-109">這個範例會將 WinRM 監聽程式新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="edf01-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="edf01-110">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="edf01-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="edf01-111">第二個命令會將 HTTP 通訊協定 WinRM 偵聽程式新增至 VMSS 指定 URL 的憑證。</span><span class="sxs-lookup"><span data-stu-id="edf01-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="edf01-112">參數</span><span class="sxs-lookup"><span data-stu-id="edf01-112">PARAMETERS</span></span>

### <span data-ttu-id="edf01-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="edf01-113">-CertificateUrl</span></span>
<span data-ttu-id="edf01-114">指定提供新虛擬機器之憑證的連結（作為 URL）。</span><span class="sxs-lookup"><span data-stu-id="edf01-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="edf01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf01-115">-DefaultProfile</span></span>
<span data-ttu-id="edf01-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edf01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edf01-117">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="edf01-117">-Protocol</span></span>
<span data-ttu-id="edf01-118">指定 WinRM 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="edf01-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="edf01-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="edf01-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="edf01-120">Http</span><span class="sxs-lookup"><span data-stu-id="edf01-120">Http</span></span>
- <span data-ttu-id="edf01-121">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="edf01-121">Https</span></span>

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

### <span data-ttu-id="edf01-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="edf01-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="edf01-123">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="edf01-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="edf01-124">您可以使用 New-AzureRmVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="edf01-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="edf01-125">-確認</span><span class="sxs-lookup"><span data-stu-id="edf01-125">-Confirm</span></span>
<span data-ttu-id="edf01-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="edf01-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf01-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf01-127">-WhatIf</span></span>
<span data-ttu-id="edf01-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edf01-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edf01-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edf01-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf01-130">CommonParameters</span></span>
<span data-ttu-id="edf01-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edf01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf01-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edf01-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf01-133">輸入</span><span class="sxs-lookup"><span data-stu-id="edf01-133">INPUTS</span></span>

## <span data-ttu-id="edf01-134">輸出</span><span class="sxs-lookup"><span data-stu-id="edf01-134">OUTPUTS</span></span>

### <span data-ttu-id="edf01-135">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="edf01-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="edf01-136">筆記</span><span class="sxs-lookup"><span data-stu-id="edf01-136">NOTES</span></span>

## <span data-ttu-id="edf01-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="edf01-137">RELATED LINKS</span></span>

[<span data-ttu-id="edf01-138">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="edf01-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


