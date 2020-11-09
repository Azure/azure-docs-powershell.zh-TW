---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284592"
---
# <span data-ttu-id="7c0f6-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7c0f6-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="7c0f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0f6-103">支援針對 SAP 系統進行監控。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="7c0f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c0f6-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c0f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c0f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0f6-106">AzVMAEMExtension Cmdlet 會更新虛擬機器的 **設定** ，以啟用或更新在虛擬機器上安裝之 SAP 系統的監視支援。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="7c0f6-107">此 Cmdlet 會安裝 Azure 增強型監視 (AEM) 擴充，可收集效能資料，並在 SAP 系統中可供探索。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="7c0f6-108">示例</span><span class="sxs-lookup"><span data-stu-id="7c0f6-108">EXAMPLES</span></span>

### <span data-ttu-id="7c0f6-109">範例1：使用 AEM 延伸功能</span><span class="sxs-lookup"><span data-stu-id="7c0f6-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="7c0f6-110">這個命令會將名為 contoso-server 的虛擬機器設定為使用 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="7c0f6-111">此命令會指定名為 stdstorage 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="7c0f6-112">參數</span><span class="sxs-lookup"><span data-stu-id="7c0f6-112">PARAMETERS</span></span>

### <span data-ttu-id="7c0f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0f6-113">-DefaultProfile</span></span>
<span data-ttu-id="7c0f6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c0f6-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="7c0f6-115">-EnableWAD</span></span>
<span data-ttu-id="7c0f6-116">如果提供此參數，則 commandlet 會針對此虛擬機器啟用 Windows Azure 診斷。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="7c0f6-117">-InstallNewExtension</span></span>
<span data-ttu-id="7c0f6-118">安裝適用于 SAP 的新 VM 延伸。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c0f6-119">-NoWait</span></span>
<span data-ttu-id="7c0f6-120">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7c0f6-121">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7c0f6-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="7c0f6-122">-OSType</span></span>
<span data-ttu-id="7c0f6-123">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="7c0f6-124">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="7c0f6-125">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c0f6-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c0f6-127">指定此 Cmdlet 修改之虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7c0f6-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="7c0f6-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="7c0f6-129">將 VM 身分識別的存取權設定為個別資源（例如，資料磁片，而不是完整的資源群組）。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="7c0f6-130">-SkipStorage</span></span>
<span data-ttu-id="7c0f6-131">表示此 Cmdlet 會跳過儲存空間的設定。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c0f6-132">-VMName</span></span>
<span data-ttu-id="7c0f6-133">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7c0f6-134">這個 Cmdlet 會為此參數指定的虛擬機器新增 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c0f6-135">-WADStorageAccountName</span></span>
<span data-ttu-id="7c0f6-136">指定此 Cmdlet 用來設定 LinuxDiagnostics 或 IaaSDiagnostics 延伸的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="7c0f6-137">如果虛擬機器不使用標準儲存空間帳戶，您必須指定此參數的值。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0f6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0f6-138">CommonParameters</span></span>
<span data-ttu-id="7c0f6-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0f6-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7c0f6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0f6-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7c0f6-141">INPUTS</span></span>

### <span data-ttu-id="7c0f6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="7c0f6-142">System.String</span></span>

## <span data-ttu-id="7c0f6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7c0f6-143">OUTPUTS</span></span>

### <span data-ttu-id="7c0f6-144">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7c0f6-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7c0f6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7c0f6-145">NOTES</span></span>

## <span data-ttu-id="7c0f6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c0f6-146">RELATED LINKS</span></span>

[<span data-ttu-id="7c0f6-147">AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7c0f6-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="7c0f6-148">移除-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7c0f6-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="7c0f6-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7c0f6-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


