---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 4784df2e4ab6d24923bb4c7619e18459101bdf41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915597"
---
# <span data-ttu-id="77f08-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="77f08-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="77f08-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77f08-102">SYNOPSIS</span></span>
<span data-ttu-id="77f08-103">啟用 SAP 系統監控的支援。</span><span class="sxs-lookup"><span data-stu-id="77f08-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="77f08-104">語法</span><span class="sxs-lookup"><span data-stu-id="77f08-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77f08-105">描述</span><span class="sxs-lookup"><span data-stu-id="77f08-105">DESCRIPTION</span></span>
<span data-ttu-id="77f08-106">**Set-AzVMAEMExtension** Cmdlet 會更新虛擬機器的設定，以啟用或更新監控安裝在虛擬機器上的 SAP 系統的支援。</span><span class="sxs-lookup"><span data-stu-id="77f08-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="77f08-107">Cmdlet 會安裝 Azure 增強型 (AEM) 擴充功能，可收集績效資料，使其可于 SAP 系統上探索。</span><span class="sxs-lookup"><span data-stu-id="77f08-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="77f08-108">例子</span><span class="sxs-lookup"><span data-stu-id="77f08-108">EXAMPLES</span></span>

### <span data-ttu-id="77f08-109">範例 1：使用 AEM 擴充功能</span><span class="sxs-lookup"><span data-stu-id="77f08-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="77f08-110">此命令會設定名為 contoso-server 的虛擬機器，以使用 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="77f08-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="77f08-111">命令會指定名為 stdstorage 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="77f08-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="77f08-112">參數</span><span class="sxs-lookup"><span data-stu-id="77f08-112">PARAMETERS</span></span>

### <span data-ttu-id="77f08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f08-113">-DefaultProfile</span></span>
<span data-ttu-id="77f08-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="77f08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f08-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="77f08-115">-EnableWAD</span></span>
<span data-ttu-id="77f08-116">如果提供此參數，Commandlet 會為此虛擬機器啟用 Windows Azure 診斷。</span><span class="sxs-lookup"><span data-stu-id="77f08-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="77f08-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="77f08-117">-InstallNewExtension</span></span>
<span data-ttu-id="77f08-118">安裝 SAP 的新 VM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="77f08-118">Install the new VM Extension for SAP.</span></span>

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

### <span data-ttu-id="77f08-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="77f08-119">-NoWait</span></span>
<span data-ttu-id="77f08-120">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="77f08-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="77f08-121">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="77f08-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="77f08-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="77f08-122">-OSType</span></span>
<span data-ttu-id="77f08-123">指定作業系統磁片的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="77f08-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="77f08-124">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="77f08-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="77f08-125">此參數可接受的值為：Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="77f08-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="77f08-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f08-126">-ResourceGroupName</span></span>
<span data-ttu-id="77f08-127">指定此 Cmdlet 修改之虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="77f08-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="77f08-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="77f08-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="77f08-129">設定對個別資源的 VM 身分識別存取權，例如資料磁片，而非完整的資源群組。</span><span class="sxs-lookup"><span data-stu-id="77f08-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

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

### <span data-ttu-id="77f08-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="77f08-130">-SkipStorage</span></span>
<span data-ttu-id="77f08-131">表示此 Cmdlet 略過儲存空間的組配置。</span><span class="sxs-lookup"><span data-stu-id="77f08-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="77f08-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="77f08-132">-VMName</span></span>
<span data-ttu-id="77f08-133">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="77f08-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="77f08-134">此 Cmdlet 會新增此參數指定之虛擬機器的 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="77f08-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="77f08-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="77f08-135">-WADStorageAccountName</span></span>
<span data-ttu-id="77f08-136">指定此 Cmdlet 用來設定 LinuxDiagnostics 或IaaSDiagnostics 擴充功能之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="77f08-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="77f08-137">如果虛擬機器不使用標準儲存空間帳戶，您必須為此參數指定值。</span><span class="sxs-lookup"><span data-stu-id="77f08-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="77f08-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f08-138">CommonParameters</span></span>
<span data-ttu-id="77f08-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77f08-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f08-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77f08-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f08-141">輸入</span><span class="sxs-lookup"><span data-stu-id="77f08-141">INPUTS</span></span>

### <span data-ttu-id="77f08-142">System.String</span><span class="sxs-lookup"><span data-stu-id="77f08-142">System.String</span></span>

## <span data-ttu-id="77f08-143">輸出</span><span class="sxs-lookup"><span data-stu-id="77f08-143">OUTPUTS</span></span>

### <span data-ttu-id="77f08-144">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="77f08-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="77f08-145">筆記</span><span class="sxs-lookup"><span data-stu-id="77f08-145">NOTES</span></span>

## <span data-ttu-id="77f08-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="77f08-146">RELATED LINKS</span></span>

[<span data-ttu-id="77f08-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="77f08-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="77f08-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="77f08-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="77f08-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="77f08-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


