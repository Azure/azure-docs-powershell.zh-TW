---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: edc91b756b90684299d84228c04862a0ce6c2e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444699"
---
# <span data-ttu-id="6cb45-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6cb45-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="6cb45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cb45-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb45-103">支援針對 SAP 系統進行監控。</span><span class="sxs-lookup"><span data-stu-id="6cb45-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cb45-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cb45-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [<CommonParameters>]
```

## <span data-ttu-id="6cb45-105">說明</span><span class="sxs-lookup"><span data-stu-id="6cb45-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb45-106">AzureRmVMAEMExtension Cmdlet 會更新虛擬機器的 **設定** ，以啟用或更新在虛擬機器上安裝之 SAP 系統的監視支援。</span><span class="sxs-lookup"><span data-stu-id="6cb45-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="6cb45-107">此 Cmdlet 會安裝 Azure 增強型監視 (AEM) 擴充，可收集效能資料，並在 SAP 系統中可供探索。</span><span class="sxs-lookup"><span data-stu-id="6cb45-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="6cb45-108">示例</span><span class="sxs-lookup"><span data-stu-id="6cb45-108">EXAMPLES</span></span>

### <span data-ttu-id="6cb45-109">範例1：使用 AEM 延伸功能</span><span class="sxs-lookup"><span data-stu-id="6cb45-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="6cb45-110">這個命令會將名為 contoso-server 的虛擬機器設定為使用 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="6cb45-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="6cb45-111">此命令會指定名為 stdstorage 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="6cb45-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="6cb45-112">參數</span><span class="sxs-lookup"><span data-stu-id="6cb45-112">PARAMETERS</span></span>

### <span data-ttu-id="6cb45-113">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="6cb45-113">-DisableWAD</span></span>
<span data-ttu-id="6cb45-114">表示此 Cmdlet 不會啟用虛擬機器的 Azure 診斷。</span><span class="sxs-lookup"><span data-stu-id="6cb45-114">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="6cb45-115">-EnableWAD</span></span>
<span data-ttu-id="6cb45-116">如果提供此參數，則 commandlet 會針對此虛擬機器啟用 Windows Azure 診斷。</span><span class="sxs-lookup"><span data-stu-id="6cb45-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="6cb45-117">-OSType</span></span>
<span data-ttu-id="6cb45-118">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="6cb45-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="6cb45-119">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6cb45-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="6cb45-120">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="6cb45-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb45-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cb45-122">指定此 Cmdlet 修改之虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cb45-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="6cb45-123">-SkipStorage</span></span>
<span data-ttu-id="6cb45-124">表示此 Cmdlet 會跳過儲存空間的設定。</span><span class="sxs-lookup"><span data-stu-id="6cb45-124">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="6cb45-125">-VMName</span></span>
<span data-ttu-id="6cb45-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cb45-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6cb45-127">這個 Cmdlet 會為此參數指定的虛擬機器新增 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="6cb45-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6cb45-128">-WADStorageAccountName</span></span>
<span data-ttu-id="6cb45-129">指定此 Cmdlet 用來設定 LinuxDiagnostics 或 IaaSDiagnostics 延伸的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6cb45-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="6cb45-130">如果虛擬機器不使用標準儲存空間帳戶，您必須指定此參數的值。</span><span class="sxs-lookup"><span data-stu-id="6cb45-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb45-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb45-131">CommonParameters</span></span>
<span data-ttu-id="6cb45-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cb45-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb45-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6cb45-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb45-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6cb45-134">INPUTS</span></span>

### <span data-ttu-id="6cb45-135">所有</span><span class="sxs-lookup"><span data-stu-id="6cb45-135">None</span></span>
<span data-ttu-id="6cb45-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6cb45-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cb45-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6cb45-137">OUTPUTS</span></span>

## <span data-ttu-id="6cb45-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6cb45-138">NOTES</span></span>

## <span data-ttu-id="6cb45-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cb45-139">RELATED LINKS</span></span>

[<span data-ttu-id="6cb45-140">AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6cb45-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="6cb45-141">移除-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6cb45-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="6cb45-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6cb45-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)

